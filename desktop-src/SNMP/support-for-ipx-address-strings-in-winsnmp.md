---
title: Suporte para cadeias de caracteres de Endereço IPX em WinSNMP
description: WinSNMP 2,0 formalizes o uso de cadeias de caracteres de Endereço IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634839"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a>Suporte para cadeias de caracteres de Endereço IPX em WinSNMP

WinSNMP 2,0 formalizes o uso de cadeias de caracteres de Endereço IPX. Se você especificar uma cadeia de caracteres de Endereço IPX como um parâmetro de entrada para a função [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) , deverá Formatar a cadeia de caracteres usando os seguintes padrões:

-   Um número de rede que consiste em oito dígitos hexadecimais (preenchido com zero, se necessário)
-   Um separador (":", "." ou "–")
-   Um número de nó que consiste em 12 dígitos hexadecimais (preenchido com zero, se necessário)

Por exemplo, 00000001:00081A0D01C2 ou 00000001.00081 a0d01c2. Os dígitos hexadecimais podem ser maiúsculos ou minúsculos.

Esse é o formato que a função [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) usa para retornar uma cadeia de caracteres de Endereço IPX. A cadeia de caracteres é retornada quando um aplicativo que está operando em um dos \_ modos não traduzidos do snmpapi chama a função **SnmpEntityToStr** . A cadeia de caracteres também pode ser retornada quando o aplicativo estiver operando no \_ modo traduzido do snmpapi e nenhum nome amigável estiver disponível para a entidade.

 

 




