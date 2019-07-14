{\rtf1\ansi\ansicpg1252\cocoartf1671\cocoasubrtf400
{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww14380\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 Pipeline\
\{\
	agent any\
		stages\
		\{\
			stage(\'91One\'92)\
			\{\
				echo \'91Hi, this is Sudarsana\'92\
			\}\
			stage(\'92Two\'92)\
				\{\
				steps\
					\{\
					input(\'91Do you want to proceed ?\'92)\
					\}\
				\}\
			stage(\'92Three\'92)\
			\{\
				parallel\
				\{\
					stage(\'91Unit Test\'92)\
						\{\
						steps\
							\{\
							echo \'93Running the unit test\'94\
							\}\
						\}\
					stage(\'91Integration Test\'92)\
						\{\
							agent\
							\{\
								docker\
								\{\
									reuseNode false\
									image \'91ubuntu\'92\
								\}\
							\}\
							steps\
								\{\
								echo \'91Running the Integration test\'92\
								\}\
						\}			\
\
				\}\
			\}\
		\}\
\}}