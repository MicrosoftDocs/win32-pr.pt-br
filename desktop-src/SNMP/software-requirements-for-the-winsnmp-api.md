---
title: Requisitos de software para a API WinSNMP
description: Um aplicativo WinSNMP deve acessar a API winSNMP por meio da biblioteca de vínculo dinâmico WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cf78c4937996a44b2a82ebeb0b2963f9a4ffaada0288068b07cd3b60432c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886066"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Requisitos de software para a API WinSNMP

Um aplicativo WinSNMP deve acessar a API winSNMP por meio da biblioteca de vínculo dinâmico WSNMP32.DLL.

Os arquivos a seguir são necessários para dar suporte à funcionalidade da API WinSNMP.



| Nome de arquivo     | Descrição                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32. Lib  | Biblioteca WinSNMP                                                                              |
| WSNMP32.DLL  | Fornece a interface WinSNMP                                                                   |
| WINSNMP. H    | Arquivo de título WinSNMP                                                                          |
| SNMPTRAP.EXE | Recebe interceptações SNMP e encaminha-as para MGMTAPI.DLL, a biblioteca de API do Microsoft SNMP Manager |
| SNMPAPI.DLL  | Fornece utilitários SNMP                                                                      |



 

 

 




