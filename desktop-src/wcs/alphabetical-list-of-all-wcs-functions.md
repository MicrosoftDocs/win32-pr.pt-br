---
title: Lista alfabética de todas as funções do WCS
description: veja a seguir uma lista alfabética completa das funções de API WCS 1,0 fornecidas pelo Windows \ 160; 98 e posterior e Windows \ 160; 2000 e posterior.
ms.assetid: aba45dbd-6fc2-4788-87f0-043579fa53f9
keywords:
- Windows Sistema de cores (WCS), funções
- WCS (Windows sistema de cores), funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- cores, funções
- Referência do WCS, funções
- referência para WCS, funções
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e2c9250cc9fb1e9e418079ed3b9524b3add2535dd780eed65ae998bda80ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706656"
---
# <a name="alphabetical-list-of-all-wcs-functions"></a>Lista alfabética de todas as funções do WCS

veja a seguir uma lista alfabética completa das funções de API WCS 1,0 fornecidas pelo Windows 98 e posterior e Windows 2000 e posterior.



| Função ou estrutura                                                                 | Descrição                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (ou **ApplyCallbackFunction**) é uma função de retorno de chamada que você implementa que atualiza os dados de configuração do WCS enquanto a caixa de diálogo exibida pela função [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) está em execução. |
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Associa um perfil de cor especificado a um dispositivo especificado.                                                                                                            |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Verifica se os pixels em um bitmap especificado estão dentro da [gama](g.md) de saída de uma transformação especificada. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina se as cores em uma matriz ficam dentro da [gama](g.md) de saída de uma transformação especificada. |
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                                       | Verifica se as cores determinadas estão na gama de um dispositivo.                                                                                                      |
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Fecha um identificador de perfil aberto. |
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Determina se as cores determinadas estão dentro da [gama](./g.md) de saída de uma transformação especificada. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Determina se as corridas de RGB especificadas ficam na [gama](./g.md) de saída de uma transformação especificada. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                                     | Verifica as cores de bitmap em uma gama de saída.                                                                                                        |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Converte nomes de cores em um espaço de cores nomeado para indexar números em um perfil de cor |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transforma índices em um espaço de cores em uma matriz de nomes em um espaço de cores nomeado. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Cria um [perfil de link de dispositivo](./d.md) no formato especificado pelo consórcio de cor internacional em sua especificação de formato de perfil ICC. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Aceita uma matriz de perfis ou um único [perfil de link de dispositivo](./d.md) e cria uma transformação de cor. Essa transformação é um mapeamento do espaço de cores especificado pelo primeiro perfil para o do segundo perfil e assim por diante para o último. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Cria um perfil de cor de exibição de uma estrutura [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) . |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Cria um perfil de cor de exibição de uma estrutura [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) . |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | Preterido. Não há uma API de substituição porque esta não estava mais sendo usada. Os desenvolvedores de módulos do CMM alternativos não são necessários para implementá-lo. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Cria uma transformação de cor que mapeia de um [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) de entrada para um espaço de destino opcional e, em seguida, para um dispositivo de saída, usando um conjunto de sinalizadores que definem como a transformação deve ser criada. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Cria uma transformação de cor que mapeia de um [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) de entrada para um espaço de destino opcional e, em seguida, para um dispositivo de saída, usando um conjunto de sinalizadores que definem como a transformação deve ser criada. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | Preterido. Não há uma API de substituição porque esta não estava mais sendo usada. Os desenvolvedores de módulos do CMM alternativos não são necessários para implementá-lo. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Exclui uma transformação de cor especificada e libera qualquer memória associada a ela. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Recupera várias informações sobre o módulo de gerenciamento de cores (CMM). |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Recupera informações sobre o perfil de cor nomeada especificado. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/)           | obtém um dicionário de renderização de cor PostScript.                                                                                                        |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | recupera a [tentativa de renderização](rendering-intents.md) de cor PostScript nível 2 de um perfil. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                             | obtém uma matriz de espaço de cor PostScript.                                                                                                                 |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Relata se o perfil fornecido é um perfil ICC válido que pode ser usado para o gerenciamento de cores. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Traduz uma matriz de cores de um [espaço de cor](color-spaces.md) de origem para um espaço de cores de destino usando uma transformação de cor. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Traduz um RGBQuad fornecido pelo aplicativo no [espaço de cores](color-spaces.md)do dispositivo. |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Traduz um bitmap de um espaço de [cor](color-spaces.md) para outro usando uma transformação de cor. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Converte um bitmap de um formato definido em um formato definido diferente e chama periodicamente uma função de retorno de chamada, se um for especificado, para relatar o progresso e permitir que o aplicativo de chamada encerre a tradução. |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                                     | Corrige as entradas em uma paleta para um contexto de dispositivo.                                                                                              |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                                       | Executa o mapeamento de cores para fins de visualização.                                                                                                         |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Converte nomes de cores em um espaço de cores nomeado para indexar números em um perfil de cores ICC (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transforma índices em um espaço de cores em uma matriz de nomes em um espaço de cores nomeado. |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                                           | Cria um espaço de cores.                                                                                                                               |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransforma) | Transforma índices em um espaço de cores em uma matriz de nomes em um espaço de cores nomeado. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transforma índices em um espaço de cores em uma matriz de nomes em um espaço de cores nomeado. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Aceita uma matriz de perfis ou um único [perfil de link de dispositivo](d.md) e cria uma transformação de cor que os aplicativos podem usar para executar o mapeamento de cores. |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Converte um [espaço de cor](c.md) lógico em um [perfil de dispositivo](d.md). |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                                           | Exclui um espaço de cores.                                                                                                                               |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Exclui uma determinada transformação de cor. |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Desassocia um perfil de cor especificado com um dispositivo especificado em um computador especificado. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera todos os perfis que satisfazem os critérios de enumeração determinados. |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                                             | Enumera os perfis de cor de saída disponíveis para um determinado contexto de dispositivo.                                                                               |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/)                     | Função de retorno de chamada definida pelo aplicativo [**para EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).                                                                |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera várias informações sobre o CMM (módulo de gerenciamento de cores) que criou a transformação de cor especificada. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Recupera o caminho do diretório Windows COLOR em um computador especificado. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia dados de um elemento de perfil marcado especificado de um perfil de cor especificado em um buffer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera o nome da marca especificado por *dwIndex* na tabela de marca de um determinado perfil de cor do ICC (International Color Consortium), em que *dwIndex* é um índice de base única nessa tabela. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/getcolorprofilefromhandle)                         | Recupera o conteúdo do perfil de cor dado um alça para um perfil de cor aberto.                                                                        |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera ou deriva a estrutura de título ICC do perfil de cor ICC ou do perfil XML do WCS. Drivers e aplicativos devem assumir que **retornar TRUE** indica apenas que um header estruturado corretamente é retornado. Cada marca ainda precisará ser validada independentemente usando APIs ICM2 herdadas ou APIs de esquema XML. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Obtém o espaço de cor de entrada atual em um contexto de dispositivo. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera o número de elementos marcados em um determinado perfil de cor. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Obtém a rampa gama de placas de exibição de cores diretas.                                                                                                |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                                                 | Obtém o perfil de cor de saída atual de um contexto de dispositivo.                                                                                           |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                                           | Obtém a [**estrutura LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) de um contexto de dispositivo.                                                                       |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera informações sobre o perfil de cor nomeado do ICC (International Color Consortium) especificado no primeiro parâmetro. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera o dicionário PostScript renderização de cores nível 2 do perfil de cor ICC especificado. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera a intenção PostScript renderização de cor de nível 2 [de](r.md) um perfil de cor ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera a matriz PostScript de espaço [de](c.md) cor nível 2 de um perfil de cor ICC. |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera o perfil de cor registrado para o espaço de [cor padrão especificado.](c.md) |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)                             | Retorno de chamada fornecido pelo aplicativo para relatar o progresso.                                                                                                    |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Instala um determinado perfil para uso em um computador especificado. O perfil também é copiado para o diretório COLOR. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Informa se uma marca ICC (International Color Consortium) especificada está presente no perfil de cor especificado. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Permite que você determine se o perfil especificado é um perfil válido do ICC (International Color Consortium) ou um handle de perfil do WCS (Sistema de Cores do Windows) válido que pode ser usado para o gerenciamento de cores. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Cria um alça para um perfil de cor especificado. O handle pode ser usado em outras funções de gerenciamento de perfil. |
| [**RegistrarCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Associa um valor de identificação especificado à biblioteca de vínculo dinâmico (CMM DLL) do módulo de gerenciamento de cores especificado. Quando essa ID aparece em um perfil de cor, Windows pode localizar o CMM correspondente para criar uma transformação. |
| [**SelecioneCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Permite que você selecione o CMM (módulo de gerenciamento de cores) preferencial a ser usado. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Define os dados do elemento para um elemento de perfil marcado em um perfil de cor ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Cria em um perfil de cor ICC especificado uma nova marca que faz referência aos mesmos dados de uma marca existente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Define o tamanho de um elemento marcado em um perfil de cor ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Define os dados de header em um perfil de cor ICC especificado. |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                                                 | Define o espaço de cor de entrada de um contexto de dispositivo.                                                                                                           |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Define a rampa gama em placas de exibição de cores diretas.                                                                                                  |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                                       | Liga ou desliga o gerenciamento de cores em um contexto de dispositivo.                                                                                                |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                                                 | Define o perfil de cor de saída para um determinado contexto de dispositivo.                                                                                            |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra um perfil especificado para um determinado espaço de [cor padrão.](c.md) O perfil pode ser consultado usando [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                                       | Fornece controle do usuário sobre o gerenciamento de cores por meio de uma caixa de diálogo.                                                                                  |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                                     | Converte cores de bitmap usando uma transformação de cor.                                                                                                      |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Converte uma matriz de cores do espaço de cores de [origem](c.md) para o espaço de cores de destino, conforme definido por uma transformação de cor. |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Remove um perfil de cor especificado de um computador especificado. Os arquivos associados são, opcionalmente, excluídos do sistema. |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Desassocia um valor de ID especificado de uma determinada biblioteca de vínculo dinâmico (CMM DLL) do módulo de gerenciamento de cores. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Associa um perfil de cor WCS especificado a um dispositivo especificado.                                                                                    |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                                               | Determina se as cores em uma matriz estão dentro da gama de saída de uma transformação de cor WCS especificada.                                            |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Converte um perfil WCS em um perfil ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Desassocia um perfil de cor do WCS especificado com um dispositivo especificado em um computador especificado.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera todos os perfis de cores que atendem aos critérios de enumeração no escopo de gerenciamento de perfil especificado.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) | Retorna o tamanho, em bytes, do buffer exigido pela [**função WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) para enumerar perfis de cores. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina se o gerenciamento do sistema do estado de calibragem de exibição está habilitado.                                                                    |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) | Recupera o perfil de cor padrão para um dispositivo ou o padrão independente do dispositivo se o dispositivo não for especificado.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Retorna o tamanho, em bytes, do nome do perfil de cor padrão para um dispositivo, incluindo o terminador **NULL.**                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Retorna a intenção de renderização de todo o sistema ou usuário.                                                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina se o usuário optou por usar uma lista de associação de perfil por usuário para o dispositivo especificado.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Cria um alça para um perfil de cor especificado.                                                                                                       |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Habilita ou desabilita o gerenciamento do sistema do estado de calibragem de exibição.                                                                              |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Define o nome do perfil de cor padrão do tipo de perfil especificado no escopo de gerenciamento de perfil especificado.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Define a intenção de renderização de todo o sistema ou usuário.                                                                                                       |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Permite que o usuário especifique se deve ou não usar uma lista de associação de perfil por usuário para o dispositivo especificado.                                       |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Converte uma matriz de cores do espaço de cores de origem para o espaço de cores de destino, conforme definido por uma transformação de cor.                            |



 

 

 