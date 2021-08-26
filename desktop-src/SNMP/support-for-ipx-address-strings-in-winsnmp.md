---
title: Suporte para cadeias de caracteres de endereço IPX no WinSNMP
description: O WinSNMP 2.0 formaliza o uso de cadeias de caracteres de endereço IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: debd25897c32515b880ff82f691aa0421af6358ae72c7e49de3408d55bcbd609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886076"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a>Suporte para cadeias de caracteres de endereço IPX no WinSNMP

O WinSNMP 2.0 formaliza o uso de cadeias de caracteres de endereço IPX. Se você especificar uma cadeia de caracteres de endereço IPX como um parâmetro de entrada para a função [**SnmpStrToEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) deverá formatar a cadeia de caracteres usando os seguintes padrões:

-   Um número de rede que consiste em oito dígitos hexadecimais (preenchidos com zero, se necessário)
-   Um separador (":", "." ou " – ")
-   Um número de nó que consiste em 12 dígitos hexadecimais (preenchidos com zero, se necessário)

Por exemplo, 00000001:00081A0D01C2 ou 00000001.00081a0d01c2. Dígitos hexadecimais podem estar em letras maiúsculas ou minúsculas.

Esse é o formato que a [**função SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) usa para retornar uma cadeia de caracteres de endereço IPX. A cadeia de caracteres é retornada quando um aplicativo que está operando em um dos modos UNTRANSLATED SNMPAPI chama a \_ **função SnmpEntityToStr.** A cadeia de caracteres também pode ser retornada quando o aplicativo estiver operando no modo SNMPAPI TRANSLATED e nenhum nome amigável estiver \_ disponível para a entidade.

 

 




