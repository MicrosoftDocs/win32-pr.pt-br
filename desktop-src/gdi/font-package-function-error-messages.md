---
description: Mensagens de erro da função de pacote de fontes
ms.assetid: 3cf7a8a1-66b2-45ca-b53d-29c80f95ff70
title: Mensagens de erro da função de pacote de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7008707675d9b2ef3eb31229535b07b1af6000e43d1122c2929fd12988fb4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761079"
---
# <a name="font-package-function-error-messages"></a>Mensagens de erro da função de pacote de fontes

Os valores longos a seguir são retornados pelas funções de pacote de fonte ( [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage) e [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage) ) quando são encontrados erros. Quando as funções forem bem-sucedidas, o valor nenhum \_ erro será retornado.



| Valor retornado                   | Valor | Descrição                                                                                                      |
|--------------------------------|-------|------------------------------------------------------------------------------------------------------------------|
| SEM \_ erros                      | 0     | Não ocorreu nenhum erro.                                                                                               |
| formato de erro \_                    | 1006  | Ocorreu um erro de formato de dados de entrada.                                                                             |
| ERR \_ Generic                   | 1000  | Ocorreu um erro no código genérico.                                                                               |
| ERRO \_ mem                       | 1005  | Ocorreu um erro durante a alocação de memória.                                                                      |
| \_não erro sem \_ glifos                | 1009  | Nenhum glifo foi encontrado.                                                                                            |
| \_base inválida de Err \_             | 1085  | A fonte continha uma tabela de dados de linha de base inválida (BASE). Atualmente, esse valor não é usado.                      |
| ERRO \_ de \_ CMap inválido             | 1030  | A fonte continha uma tabela de mapeamento de caractere para glifos (CMap) inválida.                                           |
| ERRO \_ de \_ formato Delta inválido \_    | 1013  | Um formato Delta inválido foi detectado durante a tentativa de subconjunto de uma fonte de formato 1 ou 2.                                |
| ERRO \_ \_ EBLC inválido             | 1086  | A fonte continha uma tabela de dados de local de bitmap inserida (EBLC) inválida.                                        |
| ERRO \_ \_ GLYF inválido             | 1061  | A fonte continha uma tabela de dados de glifo (glyf) inválida.                                                           |
| ERRO \_ \_ GDEF inválido             | 1083  | A fonte continha uma tabela inválida de dados de definição de glifos (GDEF). Atualmente, esse valor não é usado.              |
| ERRO de \_ GPOs inválidos \_             | 1082  | A fonte continha uma tabela de dados de posicionamento de glifos (GPOS) inválida. Atualmente, esse valor não é usado.             |
| ERRO \_ \_ GSUB inválido             | 1081  | A fonte continha uma tabela inválida de dados de substituição de glifo (GSUB).                                              |
| ERRO \_ \_ HDMX inválido             | 1089  | A fonte continha uma tabela de métricas de dispositivo horizontal (hdmx) inválida.                                            |
| \_cabeça inválida de Err \_             | 1062  | A fonte continha uma tabela inválida de cabeçalho de fonte (cabeçalho).                                                          |
| ERRO \_ \_ HHEA inválido             | 1063  | A fonte continha uma tabela de cabeçalho horizontal inválida (hhea).                                                    |
| ERR \_ \_ HHEA \_ ou \_ VHEA inválido   | 1072  | A fonte continha uma tabela inválida de cabeçalho horizontal (hhea) ou uma tabela vhea (cabeçalho de métrica vertical) inválida. |
| ERRO \_ \_ HMTX inválido             | 1064  | A fonte continha uma tabela de métricas horizontais (hmtx) inválida.                                                   |
| ERR \_ \_ HMTX \_ ou \_ VMTX inválido   | 1073  | A fonte continha uma tabela de métricas horizontais (hmtx) inválida ou uma tabela de vmtx (métrica vertical inválida).       |
| ERRO \_ \_ JSTF inválido             | 1084  | A fonte continha uma tabela de dados de justificativa (JSTF) inválida.                                                   |
| ERRO \_ \_ ltsh inválido             | 1087  | A fonte continha uma tabela inválida de dados de limite linear (LTSH).                                                |
| ERRO \_ \_ para inválido              | 1080  | A fonte era uma fonte TrueType aberta inválida.                                                                      |
| ERRO \_ \_ VDMX inválido             | 1088  | A fonte continha uma tabela de métricas de dispositivo vertical (VDMX) inválida.                                              |
| ERRO \_ de \_ localizável inválido             | 1065  | A fonte continha um índice inválido para a tabela local (locais).                                                    |
| ERRO \_ \_ MAXP inválido             | 1066  | A fonte continha uma tabela de perfil máximo (maxp) inválida.                                                      |
| ERRO \_ ao \_ mesclar somas de verificação inválidas \_ | 1011  | Uma tentativa de Mesclar somas de verificação para duas fontes de uma fonte de mãe diferente não foi bem-sucedida.                       |
| ERRO \_ de \_ formatos de mesclagem inválidos \_   | 1010  | Uma tentativa de Mesclar fontes com os formatos de dttf incorretos não foi bem-sucedida.                                          |
| ERRO \_ de \_ mesclagem inválido \_ NUMGLYPHS | 1012  | Uma tentativa de mesclar o número de glifos para duas fontes de uma fonte de mãe diferente não foi bem-sucedida.            |
| \_nome inválido de erro \_             | 1067  | O nome do pacote de fontes ou um nome de fonte era inválido.                                                                |
| ERRO \_ \_ post inválido             | 1068  | A fonte continha uma tabela PostScript (postagem) inválida.                                               |
| ERR \_ INVALID \_ OS2              | 1069  | A fonte continha uma tabela de métricas específicas do sistema operacional/2 Windows (OS/2) inválidas.                                    |
| ERR \_ \_ VHEA INVÁLIDO             | 1070  | A fonte continha uma tabela vhea (header de métricas verticais) inválida.                                              |
| ERR \_ \_ VMTX INVÁLIDO             | 1071  | A fonte continha uma tabela de métricas verticais inválidas (vmtx).                                                     |
| ERR \_ INVALID \_ TTC \_ INDEX       | 1015  | Um índice TTC (baseado em zero) inválido no arquivo de fonte foi passado.                                                 |
| ERR \_ MISSING \_ CMAP             | 1030  | A fonte não continha uma tabela cmap.                                                                           |
| ERR \_ MISSING \_ EBDT             | 1044  | A fonte não continha uma tabela EBDT.                                                                          |
| ERR \_ MISSING \_ GLYF             | 1031  | A fonte não continha uma tabela glif.                                                                           |
| ERR \_ MISSING \_ HEAD             | 1032  | A fonte não continha uma tabela de cabeça.                                                                           |
| ERR \_ MISSING \_ HHEA             | 1046  | A fonte não continha uma tabela hhea.                                                                          |
| ERR \_ MISSING \_ HMTX             | 1034  | A fonte não continha uma tabela hmtx.                                                                          |
| ERR \_ MISSING \_ LOCA             | 1035  | A fonte não continha uma tabela de localização.                                                                           |
| ERRO \_ \_ MAXP AUSENTE             | 1036  | A fonte não continha uma tabela maxp.                                                                           |
| ERR \_ MISSING \_ NAME             | 1037  | A fonte não continha uma tabela de nomeação (nome).                                                                  |
| ERR \_ MISSING \_ POST             | 1038  | A fonte não continha uma tabela de postagem.                                                                           |
| ERR \_ MISSING \_ OS2              | 1039  | A fonte não continha uma tabela os/2.                                                                          |
| ERR \_ MISSING \_ VHEA             | 1040  | A fonte não continha uma tabela vhea.                                                                           |
| ERR \_ MISSING \_ VMTX             | 1041  | A fonte não continha uma tabela vmtx.                                                                           |
| ERR \_ MISSING \_ HHEA \_ OR \_ VHEA   | 1042  | A fonte não continha uma tabela hhea ou uma tabela vhea.                                                          |
| ERR \_ AUSENTE \_ HMTX \_ OU \_ VMTX   | 1043  | A fonte não continha uma tabela hmtx ou uma tabela vmtx.                                                          |
| ERR \_ NOT \_ TTC                  | 1014  | O valor fornecido não era um índice para um arquivo TTC.                                                              |
| ERR \_ PARAMETER0                | 1100  | O parâmetro de função de chamada 0 era inválido.                                                                        |
| ERR \_ PARAMETER1                | 1101  | O parâmetro de função de chamada 1 era inválido.                                                                        |
| ERR \_ PARAMETER2                | 1102  | O parâmetro de função de chamada 2 era inválido.                                                                        |
| ERR \_ PARAMETER3                | 1103  | O parâmetro de função de chamada 3 era inválido.                                                                        |
| ERR \_ PARAMETER4                | 1104  | O parâmetro de função de chamada 4 era inválido.                                                                        |
| ERR \_ PARAMETER5                | 1105  | O parâmetro de função de chamada 5 era inválido.                                                                        |
| ERR \_ PARAMETER6                | 1106  | O parâmetro de função de chamada 6 era inválido.                                                                        |
| ERR \_ PARAMETER7                | 1107  | O parâmetro de função de chamada 7 era inválido.                                                                        |
| ERR \_ PARAMETER8                | MaxPrintersPerSession을 마우스 오른쪽 단추로 클릭한 다음 수정을 클릭합니다.  | O parâmetro de função de chamada 8 era inválido.                                                                        |
| ERR \_ PARAMETER9                | 1109  | O parâmetro de função de chamada 9 era inválido.                                                                        |
| ERR \_ PARAMETER10               | 1110  | O parâmetro de função de chamada 10 era inválido.                                                                       |
| ERR \_ PARAMETER11               | 1111  | O parâmetro de função de chamada 11 era inválido.                                                                       |
| ERR \_ PARAMETER12               | 1112  | O parâmetro de função de chamada 12 era inválido.                                                                       |
| PARAMETER13 de erro \_               | Etapas de resolução para o seguinte evento ID 1113  | O parâmetro de função de chamada 13 era inválido.                                                                       |
| PARAMETER14 de erro \_               | 1114  | A chamada do parâmetro de função 14 era inválida.                                                                       |
| PARAMETER15 de erro \_               | 1115  | O parâmetro de função de chamada 15 era inválido.                                                                       |
| PARAMETER16 de erro \_               | 1116  | A chamada do parâmetro de função 16 era inválida.                                                                       |
| READCONTROL de erro \_               | 1003  | A estrutura de controle de leitura não correspondeu aos dados.                                                                   |
| READOUTOFBOUNDS de erro \_           | 1001  | Uma leitura da memória não foi permitida, possivelmente porque os dados estavam fora dos limites ou estão corrompidos.                          |
| versão de erro \_                   | 1008  | O valor de dttf. Version principal dos dados de entrada era maior que a versão que a função pode ler.                   |
| o \_ erro \_ aumentaria               | 1007  | A ação solicitada fez com que os dados aumentassem e o aplicativo deve usar dados originais.                             |
| WRITECONTROL de erro \_              | 1004  | A estrutura de controle de gravação não correspondeu aos dados.                                                                  |
| WRITEOUTOFBOUNDS de erro \_          | 1002  | Uma gravação na memória não foi permitida, possivelmente porque os dados estavam fora dos limites.                                      |



 

 

 



