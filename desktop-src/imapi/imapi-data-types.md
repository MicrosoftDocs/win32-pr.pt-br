---
title: Tipos de dados IMAPi (Imapi2. h)
description: As especificações para mídia óptica e dispositivos associados definem valores de intervalo para itens como a descrição da estrutura do DVD, a descrição das informações do disco e o tamanho da página do recurso.
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
ms.openlocfilehash: 7793bab123e2939bdc2f5a68bb705d7468da5666
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105791395"
---
# <a name="imapi-data-types"></a>Tipos de dados IMAPi

As especificações para mídia óptica e dispositivos associados definem valores de intervalo para itens como a descrição da estrutura do DVD, a descrição das informações do disco e o tamanho da página do recurso. O IMAPi define os seguintes tipos de inteiros longos não assinados (ULONG) que impõem limites de valor de intervalo. Esses tipos são definidos estritamente para validação de IDL ideal de parâmetros e como um auxílio de documentação para os chamadores em relação aos limites superiores de determinadas operações de transferência de dados disponíveis.


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
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**\_Estrutura de \_ DVD \_ IMAPI2 ULONG**                | Intervalo: 0, 65535 (0, 0x0000FFFF)<br/> A estrutura do DVD é limitada a 64 KB devido a um campo de alocação de dois bytes.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**\_ \_ Descritor do adaptador IMAPI2 ULONG \_** | Intervalo: 0, 268435455 (0, 0x0FFFFFFF)<br/> O descritor de adaptador não é implicitamente limitado.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**\_ \_ Descritor de dispositivo IMAPI2 ULONG \_**    | Intervalo: 0, 268435455 (0, 0x0FFFFFFF)<br/> O tamanho do descritor de dispositivo não é implicitamente limitado.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**\_Informações de \_ disco \_ IMAPI2 ULONG**       | Intervalo: 0, 65538 (0, 0x00010002)<br/> As informações do disco são limitadas a 64 KB mais 2 bytes para o campo tamanho.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**\_Informações de \_ controle de IMAPI2 ULONG \_**    | Intervalo: 0, 65538 (0, 0x00010002)<br/> Rastrear informações é limitado a 64 KB mais 2 bytes para o campo tamanho.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**\_Página de \_ recursos do IMAPI2 ULONG \_**                   | Intervalo: 0256 (0, 0x00000100)<br/> Uma única página de recurso é limitada a 256 bytes.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**\_Página do \_ modo \_ IMAPI2 ULONG**                            | Intervalo: 0257 (0, 0x00000101)<br/> Uma página de modo único é limitada a 257 bytes.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**\_IMAPI2 de \_ todas \_ as \_ páginas de recurso ULONG**   | Intervalo: 0, 65536 (0, 0x00010000)<br/> O número de recursos é limitado a um campo de dois bytes.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**\_IMAPI2 de \_ todos os \_ perfis ULONG**                   | Intervalo: 0, 63 (0, 0x0000003F)<br/> O número de perfis de um dispositivo é o número de perfis que se ajustam a um único recurso. Cada perfil ocupa quatro bytes. Um único recurso pode conter 252 bytes adicionais de dados, o suficiente para armazenar um máximo de 63 perfis.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**\_Páginas de \_ \_ modo IMAPI2 \_ ULONG**            | Intervalo: 0, 32763 (0, 0x00007FFB)<br/> Contagem das páginas de modo de um dispositivo. A contagem, por meio do modo \_ SENSE10, é limitada a um campo de dois bytes.<br/> O cabeçalho de parâmetro de modo é de 8 bytes. Cada página tem pelo menos dois bytes. O número máximo de páginas de modo é 32763: (65535-8)/2 arredondado para baixo.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ diferente de zero**                                   | Intervalo: 1, 2147483647 (1, 0x7FFFFFFF)<br/> Valor genérico diferente de zero que pode ser usado para verificar se um valor não é zero.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ não \_ negativo**                   | Intervalo: 0, 2147483647 (0, 0x7FFFFFFF)<br/> Um inteiro de 32 bits com valor não negativo.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Imapi2. h</dt> </dl> |



 

 





