---
title: Tipos de dados IMAPI (Imapi2.h)
description: As especificações para mídia óptica e dispositivos associados definem valores de intervalo para itens como a descrição da estrutura de DVD, a descrição das informações do disco e o tamanho da página do recurso.
ms.assetid: 8797a8d0-5ce5-4b16-9d41-c22fa0d67dcf
keywords:
- ULONG_IMAPI2_DVD_STRUCTURE
- ULONG_IMAPI2_ADAPTER_DESCRIPTOR
- ULONG_IMAPI2_DEVICE_DESCRIPTOR
- ULONG_IMAPI2_DISC_INFORMATION
- ULONG_IMAPI2_TRACK_INFORMATION
- ULONG_IMAPI2_FEATURE_PAGE
- ULONG_IMAPI2_MODE_PAGE
- ULONG_IMAPI2_ALL_FEATURE_PAGES
- ULONG_IMAPI2_ALL_PROFILES
- ULONG_IMAPI2_ALL_MODE_PAGES
- ULONG_IMAPI2_NONZERO
- ULONG_IMAPI2_NOT_NEGATIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f003c2e03ff3d21623111d3d43a83cddf43e31c64557cfce18b5a401cdcd5d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612006"
---
# <a name="imapi-data-types"></a>Tipos de dados IMAPI

As especificações para mídia óptica e dispositivos associados definem valores de intervalo para itens como a descrição da estrutura de DVD, a descrição das informações do disco e o tamanho da página do recurso. IMAPI define os seguintes tipos ULONG (inteiro longo sem sinal) que impõem limites de valor de intervalo. Esses tipos são definidos estritamente para a validação ideal de IDL de parâmetros e como um auxílio de documentação para chamadores em relação aos limites superiores para determinadas operações de transferência de dados disponíveis.


```C++
typedef ULONG ULONG_IMAPI2_DVD_STRUCTURE;
typedef ULONG ULONG_IMAPI2_ADAPTER_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DEVICE_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DISC_INFORMATION;
typedef ULONG ULONG_IMAPI2_TRACK_INFORMATION;
typedef ULONG ULONG_IMAPI2_FEATURE_PAGE;
typedef ULONG ULONG_IMAPI2_MODE_PAGE;
typedef ULONG ULONG_IMAPI2_ALL_FEATURE_PAGES;
typedef ULONG ULONG_IMAPI2_ALL_PROFILES;
typedef ULONG ULONG_IMAPI2_ALL_MODE_PAGES;
typedef ULONG ULONG_IMAPI2_NONZERO;
typedef ULONG ULONG_IMAPI2_NOT_NEGATIVE;
```





| Tipo de dados                                                                                                                                  | Descrição                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**ULONG \_ IMAPI2 \_ DVD \_ STRUCTURE**                | Intervalo: 0,65535 (0,0x0000FFFF)<br/> A estrutura de DVD é limitada a 64KB devido a um campo de alocação de dois byte.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**DESCRITOR DE ADAPTADOR \_ ULONG IMAPI2 \_ \_** | Intervalo: 0,268435455 (0,0x0FFFFFFF)<br/> O descritor do adaptador não é implicitamente limitado em tamanho.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**DESCRITOR DE DISPOSITIVO \_ ULONG IMAPI2 \_ \_**    | Intervalo: 0,268435455 (0,0x0FFFFFFF)<br/> O descritor do dispositivo não é implicitamente limitado em tamanho.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**ULONG \_ IMAPI2 \_ DISC \_ INFORMATION**       | Intervalo: 0,65538 (0,0x00010002)<br/> As informações de disco são limitadas a 64KB mais 2 bytes para o campo de tamanho.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**ULONG \_ IMAPI2 \_ TRACK \_ INFORMATION**    | Intervalo: 0,65538 (0,0x00010002)<br/> As informações de controle são limitadas a 64KB mais 2 bytes para o campo de tamanho.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**PÁGINA DE \_ RECURSOS ULONG IMAPI2 \_ \_**                   | Intervalo: 0,256 (0,0x00000100)<br/> Uma única página de recursos é limitada a 256 bytes.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**PÁGINA \_ MODO IMAPI2 ULONG \_ \_**                            | Intervalo: 0.257 (0,0x00000101)<br/> Uma página de modo único é limitada a 257 bytes.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG \_ IMAPI2 \_ ALL \_ FEATURE \_ PAGES**   | Intervalo: 0,65536 (0,0x00010000)<br/> O número de recursos é limitado a um campo de dois byte.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ IMAPI2 \_ TODOS OS \_ PERFIS**                   | Intervalo: 0,63 (0,0x0000003F)<br/> O número de perfis para um dispositivo é o número de perfis que se ajustam a um único recurso. Cada perfil ocupa quatro bytes. Um único recurso pode conter 252 bytes adicionais de dados, o suficiente para armazenar um máximo de 63 perfis.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**ULONG \_ IMAPI2 \_ ALL \_ MODE \_ PAGES**            | Intervalo: 0,32763 (0,0x00007FFB)<br/> Contagem das páginas de modo para um dispositivo. A contagem, por meio de \_ MODE SENSE10, é limitada a um campo de dois byte.<br/> O header do parâmetro de modo é de 8 bytes. Cada página tem pelo menos dois bytes. O número máximo de páginas de modo é 32763: (65535 - 8)/2 arredondado para baixo.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ NONZERO**                                   | Intervalo: 1,2147483647 (1,0x7FFFFFFF)<br/> Valor genérico não zero que pode ser usado para verificar se um valor não é zero.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ NÃO \_ NEGATIVO**                   | Intervalo: 0, 2147483647 (0,0x7FFFFFFF)<br/> Um inteiro de 32 bits com valor não negativo.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Imapi2.h</dt> </dl> |



 

 





