NATIVE_JAVA_CLASSES = \
	org.rocksdb.AbstractCompactionFilter\
	org.rocksdb.AbstractCompactionFilterFactory\
	org.rocksdb.AbstractComparator\
	org.rocksdb.AbstractEventListener\
	org.rocksdb.AbstractSlice\
	org.rocksdb.AbstractTableFilter\
	org.rocksdb.AbstractTraceWriter\
	org.rocksdb.AbstractTransactionNotifier\
	org.rocksdb.AbstractWalFilter\
	org.rocksdb.BackupEngine\
	org.rocksdb.BackupableDBOptions\
	org.rocksdb.BlockBasedTableConfig\
	org.rocksdb.BloomFilter\
	org.rocksdb.Checkpoint\
	org.rocksdb.ClockCache\
	org.rocksdb.Cache\
	org.rocksdb.CassandraCompactionFilter\
	org.rocksdb.CassandraValueMergeOperator\
	org.rocksdb.ColumnFamilyHandle\
	org.rocksdb.ColumnFamilyOptions\
	org.rocksdb.CompactionJobInfo\
	org.rocksdb.CompactionJobStats\
	org.rocksdb.CompactionOptions\
	org.rocksdb.CompactionOptionsFIFO\
	org.rocksdb.CompactionOptionsUniversal\
	org.rocksdb.CompactRangeOptions\
	org.rocksdb.ComparatorOptions\
	org.rocksdb.CompressionOptions\
	org.rocksdb.ConfigOptions\
	org.rocksdb.DBOptions\
	org.rocksdb.DirectSlice\
	org.rocksdb.Env\
	org.rocksdb.EnvOptions\
	org.rocksdb.FlushOptions\
	org.rocksdb.Filter\
	org.rocksdb.IngestExternalFileOptions\
	org.rocksdb.HashLinkedListMemTableConfig\
	org.rocksdb.HashSkipListMemTableConfig\
	org.rocksdb.HdfsEnv\
	org.rocksdb.ConcurrentTaskLimiter\
	org.rocksdb.ConcurrentTaskLimiterImpl\
	org.rocksdb.KeyMayExist\
	org.rocksdb.Logger\
	org.rocksdb.LRUCache\
	org.rocksdb.MemoryUsageType\
	org.rocksdb.MemoryUtil\
	org.rocksdb.MergeOperator\
	org.rocksdb.NativeComparatorWrapper\
	org.rocksdb.OptimisticTransactionDB\
	org.rocksdb.OptimisticTransactionOptions\
	org.rocksdb.Options\
	org.rocksdb.OptionsString\
	org.rocksdb.OptionsUtil\
	org.rocksdb.PersistentCache\
	org.rocksdb.PlainTableConfig\
	org.rocksdb.RateLimiter\
	org.rocksdb.ReadOptions\
	org.rocksdb.RemoveEmptyValueCompactionFilter\
	org.rocksdb.RestoreOptions\
	org.rocksdb.RocksCallbackObject\
	org.rocksdb.RocksDB\
	org.rocksdb.RocksEnv\
	org.rocksdb.RocksIterator\
	org.rocksdb.RocksMemEnv\
	org.rocksdb.SkipListMemTableConfig\
	org.rocksdb.Slice\
	org.rocksdb.SstFileManager\
	org.rocksdb.SstFileWriter\
	org.rocksdb.SstFileReader\
	org.rocksdb.SstFileReaderIterator\
	org.rocksdb.SstPartitionerFactory\
	org.rocksdb.SstPartitionerFixedPrefixFactory\
	org.rocksdb.Statistics\
	org.rocksdb.ThreadStatus\
	org.rocksdb.TimedEnv\
	org.rocksdb.Transaction\
	org.rocksdb.TransactionDB\
	org.rocksdb.TransactionDBOptions\
	org.rocksdb.TransactionOptions\
	org.rocksdb.TransactionLogIterator\
	org.rocksdb.TtlDB\
	org.rocksdb.VectorMemTableConfig\
	org.rocksdb.Snapshot\
	org.rocksdb.StringAppendOperator\
	org.rocksdb.UInt64AddOperator\
	org.rocksdb.WriteBatch\
	org.rocksdb.WriteBatch.Handler\
	org.rocksdb.WriteOptions\
	org.rocksdb.WriteBatchWithIndex\
	org.rocksdb.WriteBufferManager\
	org.rocksdb.WBWIRocksIterator

NATIVE_JAVA_TEST_CLASSES = \
    org.rocksdb.RocksDBExceptionTest\
    org.rocksdb.test.TestableEventListener\
    org.rocksdb.NativeComparatorWrapperTest.NativeStringComparatorWrapper\
    org.rocksdb.WriteBatchTest\
    org.rocksdb.WriteBatchTestInternalHelper

ROCKSDB_MAJOR = $(shell egrep "ROCKSDB_MAJOR.[0-9]" ../include/rocksdb/version.h | cut -d ' ' -f 3)
ROCKSDB_MINOR = $(shell egrep "ROCKSDB_MINOR.[0-9]" ../include/rocksdb/version.h | cut -d ' ' -f 3)
ROCKSDB_PATCH = $(shell egrep "ROCKSDB_PATCH.[0-9]" ../include/rocksdb/version.h | cut -d ' ' -f 3)

NATIVE_INCLUDE = ./include
ARCH := $(shell getconf LONG_BIT)
SHA256_CMD ?= sha256sum

JAVA_TESTS = \
	org.rocksdb.BackupableDBOptionsTest\
	org.rocksdb.BackupEngineTest\
	org.rocksdb.BlobOptionsTest\
	org.rocksdb.BlockBasedTableConfigTest\
	org.rocksdb.BuiltinComparatorTest\
	org.rocksdb.BytewiseComparatorRegressionTest\
	org.rocksdb.util.BytewiseComparatorTest\
	org.rocksdb.util.BytewiseComparatorIntTest\
	org.rocksdb.CheckPointTest\
	org.rocksdb.ClockCacheTest\
	org.rocksdb.ColumnFamilyOptionsTest\
	org.rocksdb.ColumnFamilyTest\
	org.rocksdb.CompactionFilterFactoryTest\
	org.rocksdb.CompactionJobInfoTest\
	org.rocksdb.CompactionJobStatsTest\
	org.rocksdb.CompactionOptionsTest\
	org.rocksdb.CompactionOptionsFIFOTest\
	org.rocksdb.CompactionOptionsUniversalTest\
	org.rocksdb.CompactionPriorityTest\
	org.rocksdb.CompactionStopStyleTest\
	org.rocksdb.ComparatorOptionsTest\
	org.rocksdb.CompressionOptionsTest\
	org.rocksdb.CompressionTypesTest\
	org.rocksdb.DBOptionsTest\
	org.rocksdb.DirectSliceTest\
	org.rocksdb.util.EnvironmentTest\
	org.rocksdb.EnvOptionsTest\
	org.rocksdb.EventListenerTest\
	org.rocksdb.HdfsEnvTest\
	org.rocksdb.IngestExternalFileOptionsTest\
	org.rocksdb.util.IntComparatorTest\
	org.rocksdb.util.JNIComparatorTest\
	org.rocksdb.FilterTest\
	org.rocksdb.FlushTest\
	org.rocksdb.InfoLogLevelTest\
	org.rocksdb.KeyMayExistTest\
	org.rocksdb.ConcurrentTaskLimiterTest\
	org.rocksdb.LoggerTest\
	org.rocksdb.LRUCacheTest\
	org.rocksdb.MemoryUtilTest\
	org.rocksdb.MemTableTest\
	org.rocksdb.MergeTest\
	org.rocksdb.MultiGetManyKeysTest\
	org.rocksdb.MultiGetTest\
	org.rocksdb.MixedOptionsTest\
	org.rocksdb.MutableColumnFamilyOptionsTest\
	org.rocksdb.MutableDBOptionsTest\
	org.rocksdb.MutableOptionsGetSetTest \
	org.rocksdb.NativeComparatorWrapperTest\
	org.rocksdb.NativeLibraryLoaderTest\
	org.rocksdb.OptimisticTransactionTest\
	org.rocksdb.OptimisticTransactionDBTest\
	org.rocksdb.OptimisticTransactionOptionsTest\
	org.rocksdb.OptionsUtilTest\
	org.rocksdb.OptionsTest\
	org.rocksdb.PlainTableConfigTest\
	org.rocksdb.RateLimiterTest\
	org.rocksdb.ReadOnlyTest\
	org.rocksdb.ReadOptionsTest\
	org.rocksdb.util.ReverseBytewiseComparatorIntTest\
	org.rocksdb.RocksDBTest\
	org.rocksdb.RocksDBExceptionTest\
	org.rocksdb.DefaultEnvTest\
	org.rocksdb.RocksIteratorTest\
	org.rocksdb.RocksMemEnvTest\
	org.rocksdb.util.SizeUnitTest\
	org.rocksdb.SecondaryDBTest\
	org.rocksdb.SliceTest\
	org.rocksdb.SnapshotTest\
	org.rocksdb.SstFileManagerTest\
	org.rocksdb.SstFileWriterTest\
	org.rocksdb.SstFileReaderTest\
	org.rocksdb.SstPartitionerTest\
	org.rocksdb.TableFilterTest\
	org.rocksdb.TimedEnvTest\
	org.rocksdb.TransactionTest\
	org.rocksdb.TransactionDBTest\
	org.rocksdb.TransactionOptionsTest\
	org.rocksdb.TransactionDBOptionsTest\
	org.rocksdb.TransactionLogIteratorTest\
	org.rocksdb.TtlDBTest\
	org.rocksdb.StatisticsTest\
	org.rocksdb.StatisticsCollectorTest\
	org.rocksdb.WalFilterTest\
	org.rocksdb.WALRecoveryModeTest\
	org.rocksdb.WriteBatchHandlerTest\
	org.rocksdb.WriteBatchTest\
	org.rocksdb.WriteBatchThreadedTest\
	org.rocksdb.WriteOptionsTest\
	org.rocksdb.WriteBatchWithIndexTest

MAIN_SRC = src/main/java
TEST_SRC = src/test/java
OUTPUT = target
MAIN_CLASSES = $(OUTPUT)/classes
TEST_CLASSES = $(OUTPUT)/test-classes
JAVADOC = $(OUTPUT)/apidocs

BENCHMARK_MAIN_SRC = benchmark/src/main/java
BENCHMARK_OUTPUT = benchmark/target
BENCHMARK_MAIN_CLASSES = $(BENCHMARK_OUTPUT)/classes

SAMPLES_MAIN_SRC = samples/src/main/java
SAMPLES_OUTPUT = samples/target
SAMPLES_MAIN_CLASSES = $(SAMPLES_OUTPUT)/classes

JAVA_TEST_LIBDIR = test-libs
JAVA_JUNIT_VER = 4.13.1
JAVA_JUNIT_SHA256 = c30719db974d6452793fe191b3638a5777005485bae145924044530ffa5f6122
JAVA_JUNIT_JAR = junit-$(JAVA_JUNIT_VER).jar
JAVA_JUNIT_JAR_PATH = $(JAVA_TEST_LIBDIR)/$(JAVA_JUNIT_JAR)
JAVA_HAMCREST_VER = 2.2
JAVA_HAMCREST_SHA256 = 5e62846a89f05cd78cd9c1a553f340d002458380c320455dd1f8fc5497a8a1c1
JAVA_HAMCREST_JAR = hamcrest-$(JAVA_HAMCREST_VER).jar
JAVA_HAMCREST_JAR_PATH = $(JAVA_TEST_LIBDIR)/$(JAVA_HAMCREST_JAR)
JAVA_MOCKITO_VER = 1.10.19
JAVA_MOCKITO_SHA256 = d1a7a7ef14b3db5c0fc3e0a63a81b374b510afe85add9f7984b97911f4c70605
JAVA_MOCKITO_JAR = mockito-all-$(JAVA_MOCKITO_VER).jar
JAVA_MOCKITO_JAR_PATH = $(JAVA_TEST_LIBDIR)/$(JAVA_MOCKITO_JAR)
JAVA_CGLIB_VER = 3.3.0
JAVA_CGLIB_SHA256 = 9fe0c26d7464140ccdfe019ac687be1fb906122b508ab54beb810db0f09a9212
JAVA_CGLIB_JAR = cglib-$(JAVA_CGLIB_VER).jar
JAVA_CGLIB_JAR_PATH = $(JAVA_TEST_LIBDIR)/$(JAVA_CGLIB_JAR)
JAVA_ASSERTJ_VER = 2.9.0
JAVA_ASSERTJ_SHA256 = 5e88ea3ecbe3c48aa1346fec76c84979fa9c8d22499f11479011691230e8babf
JAVA_ASSERTJ_JAR = assertj-core-$(JAVA_ASSERTJ_VER).jar
JAVA_ASSERTJ_JAR_PATH = $(JAVA_TEST_LIBDIR)/$(JAVA_ASSERTJ_JAR)
JAVA_TESTCLASSPATH = $(JAVA_JUNIT_JAR_PATH):$(JAVA_HAMCREST_JAR_PATH):$(JAVA_MOCKITO_JAR_PATH):$(JAVA_CGLIB_JAR_PATH):$(JAVA_ASSERTJ_JAR_PATH)

MVN_LOCAL = ~/.m2/repository

# Set the default JAVA_ARGS to "" for DEBUG_LEVEL=0
JAVA_ARGS ?=

JAVAC_ARGS ?=

# When debugging add -Xcheck:jni to the java args
ifneq ($(DEBUG_LEVEL),0)
	JAVA_ARGS += -ea -Xcheck:jni
	JAVAC_ARGS += -Xlint:deprecation -Xlint:unchecked
endif

# Using a Facebook AWS account for S3 storage. (maven.org has a history
# of failing in Travis builds.)
DEPS_URL?=https://rocksdb-deps.s3-us-west-2.amazonaws.com/jars

clean: clean-not-downloaded clean-downloaded

clean-not-downloaded:
	$(AM_V_at)rm -rf $(NATIVE_INCLUDE)
	$(AM_V_at)rm -rf $(OUTPUT)
	$(AM_V_at)rm -rf $(BENCHMARK_OUTPUT)
	$(AM_V_at)rm -rf $(SAMPLES_OUTPUT)

clean-downloaded:
	$(AM_V_at)rm -rf $(JAVA_TEST_LIBDIR)


javadocs: java
	$(AM_V_GEN)mkdir -p $(JAVADOC)
	$(AM_V_at)javadoc -d $(JAVADOC) -sourcepath $(MAIN_SRC) -subpackages org

javalib: java java_test javadocs

java:
	$(AM_V_GEN)mkdir -p $(MAIN_CLASSES)
ifeq ($(shell java -version 2>&1 | grep 1.7.0 > /dev/null; printf $$?), 0)
	$(AM_V_at)javac $(JAVAC_ARGS) -d $(MAIN_CLASSES)\
		$(MAIN_SRC)/org/rocksdb/util/*.java\
		$(MAIN_SRC)/org/rocksdb/*.java
else
	$(AM_V_at)javac $(JAVAC_ARGS) -h $(NATIVE_INCLUDE) -d $(MAIN_CLASSES)\
		$(MAIN_SRC)/org/rocksdb/util/*.java\
		$(MAIN_SRC)/org/rocksdb/*.java
endif
	$(AM_V_at)@cp ../HISTORY.md ./HISTORY-CPP.md
	$(AM_V_at)@rm -f ./HISTORY-CPP.md
ifeq ($(shell java -version 2>&1 | grep 1.7.0 > /dev/null; printf $$?), 0)
	$(AM_V_at)javah -cp $(MAIN_CLASSES) -d $(NATIVE_INCLUDE) -jni $(NATIVE_JAVA_CLASSES)
endif

sample: java
	$(AM_V_GEN)mkdir -p $(SAMPLES_MAIN_CLASSES)
	$(AM_V_at)javac $(JAVAC_ARGS) -cp $(MAIN_CLASSES) -d $(SAMPLES_MAIN_CLASSES) $(SAMPLES_MAIN_SRC)/RocksDBSample.java
	$(AM_V_at)@rm -rf /tmp/rocksdbjni
	$(AM_V_at)@rm -rf /tmp/rocksdbjni_not_found
	java $(JAVA_ARGS) -Djava.library.path=target -cp $(MAIN_CLASSES):$(SAMPLES_MAIN_CLASSES) RocksDBSample /tmp/rocksdbjni
	$(AM_V_at)@rm -rf /tmp/rocksdbjni
	$(AM_V_at)@rm -rf /tmp/rocksdbjni_not_found

column_family_sample: java
	$(AM_V_GEN)mkdir -p $(SAMPLES_MAIN_CLASSES)
	$(AM_V_at)javac $(JAVAC_ARGS) -cp $(MAIN_CLASSES) -d $(SAMPLES_MAIN_CLASSES) $(SAMPLES_MAIN_SRC)/RocksDBColumnFamilySample.java
	$(AM_V_at)@rm -rf /tmp/rocksdbjni
	java $(JAVA_ARGS) -Djava.library.path=target -cp $(MAIN_CLASSES):$(SAMPLES_MAIN_CLASSES) RocksDBColumnFamilySample /tmp/rocksdbjni
	$(AM_V_at)@rm -rf /tmp/rocksdbjni

transaction_sample: java
	$(AM_V_GEN)mkdir -p $(SAMPLES_MAIN_CLASSES)
	$(AM_V_at)javac -cp $(MAIN_CLASSES) -d $(SAMPLES_MAIN_CLASSES) $(SAMPLES_MAIN_SRC)/TransactionSample.java
	$(AM_V_at)@rm -rf /tmp/rocksdbjni
	java -ea -Xcheck:jni -Djava.library.path=target -cp $(MAIN_CLASSES):$(SAMPLES_MAIN_CLASSES) TransactionSample /tmp/rocksdbjni
	$(AM_V_at)@rm -rf /tmp/rocksdbjni

optimistic_transaction_sample: java
	$(AM_V_GEN)mkdir -p $(SAMPLES_MAIN_CLASSES)
	$(AM_V_at)javac -cp $(MAIN_CLASSES) -d $(SAMPLES_MAIN_CLASSES) $(SAMPLES_MAIN_SRC)/OptimisticTransactionSample.java
	$(AM_V_at)@rm -rf /tmp/rocksdbjni
	java -ea -Xcheck:jni -Djava.library.path=target -cp $(MAIN_CLASSES):$(SAMPLES_MAIN_CLASSES) OptimisticTransactionSample /tmp/rocksdbjni
	$(AM_V_at)@rm -rf /tmp/rocksdbjni

$(JAVA_TEST_LIBDIR):
	mkdir -p "$(JAVA_TEST_LIBDIR)"

$(JAVA_JUNIT_JAR_PATH): $(JAVA_TEST_LIBDIR)
ifneq (,$(wildcard $(MVN_LOCAL)/junit/junit/$(JAVA_JUNIT_VER)/$(JAVA_JUNIT_JAR)))
	cp -v $(MVN_LOCAL)/junit/junit/$(JAVA_JUNIT_VER)/$(JAVA_JUNIT_JAR) $(JAVA_TEST_LIBDIR)
else
	curl --fail --insecure --output $(JAVA_JUNIT_JAR_PATH) --location $(DEPS_URL)/$(JAVA_JUNIT_JAR)
	JAVA_JUNIT_SHA256_ACTUAL=`$(SHA256_CMD) $(JAVA_JUNIT_JAR_PATH) | cut -d ' ' -f 1`; \
	if [ "$(JAVA_JUNIT_SHA256)" != "$$JAVA_JUNIT_SHA256_ACTUAL" ]; then \
		echo $(JAVA_JUNIT_JAR_PATH) checksum mismatch, expected=\"$(JAVA_JUNIT_SHA256)\" actual=\"$$JAVA_JUNIT_SHA256_ACTUAL\"; \
		exit 1; \
	fi
endif

$(JAVA_HAMCREST_JAR_PATH): $(JAVA_TEST_LIBDIR)
ifneq (,$(wildcard $(MVN_LOCAL)/org/hamcrest/hamcrest/$(JAVA_HAMCREST_VER)/$(JAVA_HAMCREST_JAR)))
	cp -v $(MVN_LOCAL)/org/hamcrest/hamcrest/$(JAVA_HAMCREST_VER)/$(JAVA_HAMCREST_JAR) $(JAVA_TEST_LIBDIR)
else
	curl --fail --insecure --output $(JAVA_HAMCREST_JAR_PATH) --location $(DEPS_URL)/$(JAVA_HAMCREST_JAR)
	JAVA_HAMCREST_SHA256_ACTUAL=`$(SHA256_CMD) $(JAVA_HAMCREST_JAR_PATH) | cut -d ' ' -f 1`; \
	if [ "$(JAVA_HAMCREST_SHA256)" != "$$JAVA_HAMCREST_SHA256_ACTUAL" ]; then \
		echo $(JAVA_HAMCREST_JAR_PATH) checksum mismatch, expected=\"$(JAVA_HAMCREST_SHA256)\" actual=\"$$JAVA_HAMCREST_SHA256_ACTUAL\"; \
		exit 1; \
	fi
endif

$(JAVA_MOCKITO_JAR_PATH): $(JAVA_TEST_LIBDIR)
ifneq (,$(wildcard $(MVN_LOCAL)/org/mockito/mockito-all/$(JAVA_MOCKITO_VER)/$(JAVA_MOCKITO_JAR)))
	cp -v $(MVN_LOCAL)/org/mockito/mockito-all/$(JAVA_MOCKITO_VER)/$(JAVA_MOCKITO_JAR) $(JAVA_TEST_LIBDIR)
else
	curl --fail --insecure --output "$(JAVA_MOCKITO_JAR_PATH)" --location $(DEPS_URL)/$(JAVA_MOCKITO_JAR)
	JAVA_MOCKITO_SHA256_ACTUAL=`$(SHA256_CMD) $(JAVA_MOCKITO_JAR_PATH) | cut -d ' ' -f 1`; \
	if [ "$(JAVA_MOCKITO_SHA256)" != "$$JAVA_MOCKITO_SHA256_ACTUAL" ]; then \
		echo $(JAVA_MOCKITO_JAR_PATH) checksum mismatch, expected=\"$(JAVA_MOCKITO_SHA256)\" actual=\"$$JAVA_MOCKITO_SHA256_ACTUAL\"; \
		exit 1; \
	fi
endif

$(JAVA_CGLIB_JAR_PATH): $(JAVA_TEST_LIBDIR)
ifneq (,$(wildcard $(MVN_LOCAL)/cglib/cglib/$(JAVA_CGLIB_VER)/$(JAVA_CGLIB_JAR)))
	cp -v $(MVN_LOCAL)/cglib/cglib/$(JAVA_CGLIB_VER)/$(JAVA_CGLIB_JAR) $(JAVA_TEST_LIBDIR)
else
	curl --fail --insecure --output "$(JAVA_CGLIB_JAR_PATH)" --location $(DEPS_URL)/$(JAVA_CGLIB_JAR)
	JAVA_CGLIB_SHA256_ACTUAL=`$(SHA256_CMD) $(JAVA_CGLIB_JAR_PATH) | cut -d ' ' -f 1`; \
	if [ "$(JAVA_CGLIB_SHA256)" != "$$JAVA_CGLIB_SHA256_ACTUAL" ]; then \
		echo $(JAVA_CGLIB_JAR_PATH) checksum mismatch, expected=\"$(JAVA_CGLIB_SHA256)\" actual=\"$$JAVA_CGLIB_SHA256_ACTUAL\"; \
		exit 1; \
	fi
endif

$(JAVA_ASSERTJ_JAR_PATH): $(JAVA_TEST_LIBDIR)
ifneq (,$(wildcard $(MVN_LOCAL)/org/assertj/assertj-core/$(JAVA_ASSERTJ_VER)/$(JAVA_ASSERTJ_JAR)))
	cp -v $(MVN_LOCAL)/org/assertj/assertj-core/$(JAVA_ASSERTJ_VER)/$(JAVA_ASSERTJ_JAR) $(JAVA_TEST_LIBDIR)
else
	curl --fail --insecure --output "$(JAVA_ASSERTJ_JAR_PATH)" --location $(DEPS_URL)/$(JAVA_ASSERTJ_JAR)
	JAVA_ASSERTJ_SHA256_ACTUAL=`$(SHA256_CMD) $(JAVA_ASSERTJ_JAR_PATH) | cut -d ' ' -f 1`; \
	if [ "$(JAVA_ASSERTJ_SHA256)" != "$$JAVA_ASSERTJ_SHA256_ACTUAL" ]; then \
		echo $(JAVA_ASSERTJ_JAR_PATH) checksum mismatch, expected=\"$(JAVA_ASSERTJ_SHA256)\" actual=\"$$JAVA_ASSERTJ_SHA256_ACTUAL\"; \
		exit 1; \
	fi
endif

resolve_test_deps: $(JAVA_JUNIT_JAR_PATH) $(JAVA_HAMCREST_JAR_PATH) $(JAVA_MOCKITO_JAR_PATH) $(JAVA_CGLIB_JAR_PATH) $(JAVA_ASSERTJ_JAR_PATH)

java_test: java resolve_test_deps
	$(AM_V_GEN)mkdir -p $(TEST_CLASSES)
ifeq ($(shell java -version 2>&1|grep 1.7.0 >/dev/null; printf $$?),0)
	$(AM_V_at)javac $(JAVAC_ARGS) -cp $(MAIN_CLASSES):$(JAVA_TESTCLASSPATH) -d $(TEST_CLASSES)\
		$(TEST_SRC)/org/rocksdb/test/*.java\
		$(TEST_SRC)/org/rocksdb/util/*.java\
		$(TEST_SRC)/org/rocksdb/*.java
	$(AM_V_at)javah -cp $(MAIN_CLASSES):$(TEST_CLASSES) -d $(NATIVE_INCLUDE) -jni $(NATIVE_JAVA_TEST_CLASSES)
else
	$(AM_V_at)javac $(JAVAC_ARGS) -cp $(MAIN_CLASSES):$(JAVA_TESTCLASSPATH) -h $(NATIVE_INCLUDE) -d $(TEST_CLASSES)\
		$(TEST_SRC)/org/rocksdb/test/*.java\
		$(TEST_SRC)/org/rocksdb/util/*.java\
		$(TEST_SRC)/org/rocksdb/*.java
endif

test: java java_test run_test

run_test:
	java $(JAVA_ARGS) -Djava.library.path=target -cp "$(MAIN_CLASSES):$(TEST_CLASSES):$(JAVA_TESTCLASSPATH):target/*" org.rocksdb.test.RocksJunitRunner $(JAVA_TESTS)

db_bench: java
	$(AM_V_GEN)mkdir -p $(BENCHMARK_MAIN_CLASSES)
	$(AM_V_at)javac $(JAVAC_ARGS) -cp $(MAIN_CLASSES) -d $(BENCHMARK_MAIN_CLASSES) $(BENCHMARK_MAIN_SRC)/org/rocksdb/benchmark/*.java
