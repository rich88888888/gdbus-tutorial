
# Dbus service file
servicedir = $(DBUS_SERVICES_DIR)
service_in_files = es.aleksander.Alarm.service.in
service_DATA = $(service_in_files:.service.in=.service)
EXTRA_DIST = $(service_in_files)

# Rule to make the service file with bindir expanded
$(service_DATA): $(service_in_files) Makefile
	@sed -e "s|\@bindir\@|$(bindir)|" $<> $@

clean-local:
	rm -rf $(service_DATA)
