system_stubs_ss = ss.source_set()
system_stubs_ss.add(when: 'CONFIG_XEN', if_false: files('xen-stub.c'))
system_stubs_ss.add(when: 'CONFIG_KVM', if_false: files('kvm-stub.c'))
system_stubs_ss.add(when: 'CONFIG_TCG', if_false: files('tcg-stub.c'))
system_stubs_ss.add(when: 'CONFIG_HVF', if_false: files('hvf-stub.c'))
system_stubs_ss.add(when: 'CONFIG_NVMM', if_false: files('nvmm-stub.c'))
system_stubs_ss.add(when: 'CONFIG_WHPX', if_false: files('whpx-stub.c'))

specific_ss.add_all(when: ['CONFIG_SYSTEM_ONLY'], if_true: system_stubs_ss)
