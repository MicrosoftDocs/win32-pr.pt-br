---
description: Este tópico define as constantes de IDEFAULT de localidade \_ \* usadas pelo NLS.
ms.assetid: 4fa8b5f3-8c01-44fb-b6fd-8dbf38e3d361
title: Constantes LOCALE_IDEFAULT *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0524ea64d9924439e14ae6cb3cf16fed8a5f97ffb1e95d5f7fea98d5b6c61329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106776"
---
# <a name="locale_idefault-constants"></a>\_Constantes IDEFAULT de localidade \*

Este tópico define as constantes de IDEFAULT de localidade \_ \* usadas pelo NLS.



| Valor                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDEFAULTANSICODEPAGE de localidade \_   | A página de código ANSI usada por uma localidade para aplicativos que não dão suporte a Unicode. O número máximo de caracteres permitido para essa cadeia de caracteres é seis, incluindo um caractere nulo de terminação. Se nenhuma página de código ANSI estiver disponível, somente Unicode poderá ser usado para a localidade. Nesse caso, o valor é CP \_ ACP (0). Essa localidade não pode ser definida como a localidade do sistema. Os aplicativos que não dão suporte a Unicode não funcionam corretamente com as localidades marcadas como "somente Unicode". Para obter uma lista de ANSI e outras páginas de código, consulte [identificadores de página de código](code-page-identifiers.md). |
| IDEFAULTCODEPAGE de localidade \_       | Página de código OEM (fabricante original do equipamento) associada ao país/região. A página de código OEM é usada para conversão de aplicativos de modo de texto baseados em MS-dos. Se a localidade não usar uma página de código OEM, o valor será CP \_ OEMCP (1). O número máximo de caracteres permitido para essa cadeia de caracteres é seis, incluindo um caractere nulo de terminação. Para obter uma lista de OEM e outras páginas de código, consulte [identificadores de página de código](code-page-identifiers.md).                                                                                                               |
| IDEFAULTCOUNTRY de localidade \_        | Obsoleto. Não use. Esse valor foi fornecido para que as localidades parcialmente especificadas pudessem ser concluídas com valores padrão. As localidades parcialmente especificadas agora são preteridas.                                                                                                                                                                                                                                                                                                                                                                                               |
| IDEFAULTEBCDICCODEPAGE de localidade \_ | **Windows 2000:** Página de código de Extended Binary Coded Decimal Interchange Code padrão (EBCDIC) associada à localidade. O número máximo de caracteres permitido para essa cadeia de caracteres é seis, incluindo um caractere nulo de terminação. Para obter uma lista de EBCDIC e outras páginas de código, consulte [identificadores de página de código](code-page-identifiers.md).                                                                                                                                                                                                                                     |
| IDEFAULTLANGUAGE de localidade \_       | Obsoleto. Não use. Esse valor foi fornecido para que as localidades parcialmente especificadas pudessem ser concluídas com valores padrão. As localidades parcialmente especificadas agora são preteridas.                                                                                                                                                                                                                                                                                                                                                                                               |
| IDEFAULTMACCODEPAGE de localidade \_    | Página de código padrão do Macintosh associada à localidade. O número máximo de caracteres permitido para essa cadeia de caracteres é seis, incluindo um caractere nulo de terminação. Se a localidade não usar uma página de código do Macintosh, o valor será CP \_ MACCP (2). Para obter uma lista de Macintosh (MAC) e outras páginas de código, consulte [identificadores de página de código](code-page-identifiers.md).                                                                                                                                                                                                              |



 

 

 



