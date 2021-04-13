---
description: A seguir estão as funções da biblioteca do registro offline.
ms.assetid: 378811d2-064c-4d81-979e-392097d55baa
title: Funções da biblioteca do registro offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c36afac0b8f5f0aed17b12a7e0562cce75ea69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370380"
---
# <a name="offline-registry-library-functions"></a>Funções da biblioteca do registro offline

A seguir estão as funções da biblioteca do registro offline.



| Função                                       | Descrição                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**ORCloseHive**](orclosehive.md)             | Fecha o hive do registro offline especificado e libera a memória alocada para o hive.                                 |
| [**ORCloseKey**](orclosekey.md)               | Fecha um identificador para a chave do Registro especificada em um hive do registro offline.                                          |
| [**ORCreateHive**](orcreatehive.md)           | Cria um hive de registro offline que contém uma única chave de raiz vazia.                                             |
| [**ORCreateKey**](orcreatekey.md)             | Cria a chave do Registro especificada em um hive do registro offline. Se a chave já existir, a função a abrirá.   |
| [**ORDeleteKey**](ordeletekey.md)             | Exclui uma subchave e seus valores de um hive do registro offline.                                                      |
| [**ORDeleteValue**](ordeletevalue.md)         | Remove um valor da chave do Registro especificada em um hive do registro offline.                                        |
| [**OREnumKey**](orenumkey.md)                 | Enumera as subchaves da chave do registro aberta especificada em um hive do registro offline.                              |
| [**OREnumValue**](orenumvalue.md)             | Enumera os valores para a chave de registro aberta especificada em um hive de registro offline.                              |
| [**ORGetKeySecurity**](orgetkeysecurity.md)   | Recupera uma cópia do descritor de segurança protegendo a chave do registro aberta especificada em um hive do registro offline. |
| [**ORGetValue**](orgetvalue.md)               | Recupera o tipo e os dados para o valor do registro especificado em um hive do registro offline.                           |
| [**ORGetVersion**](orgetversion.md)           | Recupera a versão da biblioteca offline do registro.                                                              |
| [**ORGetVirtualFlags**](orgetvirtualflags.md) | Recupera os sinalizadores virtuais na chave do registro aberta especificada em um hive do registro offline.                         |
| [**OROpenHive**](oropenhive.md)               | Carrega o arquivo de Hive especificado na memória e valida o hive.                                                   |
| [**OROpenKey**](oropenkey.md)                 | Abre a chave do Registro especificada em um hive do registro offline.                                                       |
| [**ORQueryInfoKey**](orqueryinfokey.md)       | Recupera informações sobre a chave do Registro especificada em um hive do registro offline.                                 |
| [**ORSaveHive**](orsavehive.md)               | Grava o hive do registro offline especificado em um arquivo.                                                               |
| [**ORSetKeySecurity**](orsetkeysecurity.md)   | Define a segurança de uma chave do registro aberta em um hive do registro offline.                                              |
| [**ORSetValue**](orsetvalue.md)               | Define os dados para o valor de uma chave do Registro especificada em um hive do registro offline.                                |
| [**ORSetVirtualFlags**](orsetvirtualflags.md) | Define os sinalizadores de virtualização na chave do registro aberta especificada em um hive do registro offline.                           |



 

 

 



