---
title: Definindo a entidade e o modo de tradução de contexto
description: O aplicativo WinSNMP pode especificar a interpretação e a tradução de parâmetros de entidade e de contexto definindo o modo de tradução de contexto e entidade. A implementação do Microsoft WinSNMP armazena o modo em um banco de dados.
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50b5ecfb1a4703795f970f5d7c13ceaa3d64980
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005221"
---
# <a name="setting-the-entity-and-context-translation-mode"></a>Definindo a entidade e o modo de tradução de contexto

O aplicativo WinSNMP pode especificar a interpretação e a tradução de parâmetros de entidade e de contexto definindo o modo de tradução de contexto e entidade. A implementação do Microsoft WinSNMP armazena o modo em um banco de dados.

A configuração do modo de tradução de entidades e de contexto determina a maneira como a função [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) e a função [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) interpretam as cadeias de caracteres de entrada. A configuração também determina o tipo de cadeia de caracteres de saída que as funções [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) e [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) retornam. Para obter mais informações, consulte [suporte para cadeias de caracteres de Endereço IPX em WinSNMP](support-for-ipx-address-strings-in-winsnmp.md).

A implementação retorna a entidade padrão atual e o modo de tradução de contexto no parâmetro *nTranslateMode* da função [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) . Para recuperar a entidade atual e o modo de tradução de contexto em vigor para a implementação, um aplicativo pode chamar a função [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) a qualquer momento.

Os modos de validação de entidade e contexto válidos são os seguintes.

| Mode                      | Significado                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ traduzido       | A implementação usa seu banco de dados para converter nomes amigáveis de usuário para entidades SNMP e objetos gerenciados. A implementação os converte em seus componentes SNMPv1 ou SNMPv2C.                                                                                                  |
| SNMPAPI não \_ traduzido \_ v1 | A implementação interpreta os parâmetros de entidade SNMP como endereços de transporte SNMP literais e parâmetros de contexto como cadeias de caracteres da comunidade SNMP literal. Para entidades de destino SNMPv2, a implementação cria mensagens SNMP de saída que contêm um valor igual a zero no campo versão. |
| SNMPAPI não \_ traduzido \_ v2 | A implementação interpreta os parâmetros de entidade SNMP como endereços de transporte SNMP e parâmetros de contexto como cadeias de caracteres de comunidade SNMP literal. Para entidades de destino SNMPv2, a implementação cria mensagens SNMP de saída que contêm um valor de 1 no campo versão.            |



 

A implementação tenta associar recursos em seu banco de dados com o endereço de transporte literal da entidade de gerenciamento.

Para alterar a entidade e o modo de tradução do contexto, a configuração de um aplicativo WinSNMP deve chamar a função [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) . Se o modo de tradução solicitado for inválido, a função falhará e [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) retornará o código de erro snmpapi \_ modo \_ inválido.

 

 




