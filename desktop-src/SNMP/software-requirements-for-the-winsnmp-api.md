---
title: Requisitos de software para a API WinSNMP
description: Um aplicativo WinSNMP deve acessar a API WinSNMP por meio da biblioteca de vínculo dinâmico WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159286"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Requisitos de software para a API WinSNMP

Um aplicativo WinSNMP deve acessar a API WinSNMP por meio da biblioteca de vínculo dinâmico WSNMP32.DLL.

Os arquivos a seguir são necessários para dar suporte à funcionalidade da API WinSNMP.



| Nome de arquivo     | Descrição                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32. LIB  | Biblioteca WinSNMP                                                                              |
| WSNMP32.DLL  | Fornece a interface WinSNMP                                                                   |
| WINSNMP. T    | Arquivo de cabeçalho WinSNMP                                                                          |
| SNMPTRAP.EXE | Recebe interceptações SNMP e as encaminha para MGMTAPI.DLL, a biblioteca de API do Gerenciador SNMP da Microsoft |
| SNMPAPI.DLL  | Fornece utilitários SNMP                                                                      |



 

 

 




