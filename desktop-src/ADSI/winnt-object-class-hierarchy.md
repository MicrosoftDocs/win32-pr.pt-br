---
title: Hierarquia da classe de objeto WinNT
description: A hierarquia da classe de objeto WinNT começa no objeto Namespace.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- AdsI do provedor de serviços WinNT, hierarquia de classe de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e893839393ad3b9aaa42557d90f9bf279ab0625e1225ab41f2d1a3c7e7980a1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589756"
---
# <a name="winnt-object-class-hierarchy"></a>Hierarquia da classe de objeto WinNT

A hierarquia da classe de objeto WinNT começa no objeto Namespace.



| Classe Object                   | Descrição                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| Namespace<br/>           | Contêiner de objeto de nível superior.<br/>                                            |
| Domínio<br/>              | O Windows NT domínio.<br/>                                                 |
| Usuário<br/>                | Conta de usuário.<br/>                                                          |
| Agrupar<br/>               | Conta de grupo para gerenciar direitos de acesso.<br/>                              |
| UserGroupCollection<br/> | Um conjunto de grupos de usuários que [**implementam IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/>  |
| Groupcollection<br/>     | Um conjunto de outros grupos que [**implementam IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/> |
| Computador<br/>            | Windows NT servidor ou estação de trabalho 4.0.<br/>                                  |
| PrintJob<br/>            | Imprimir trabalho na fila de impressão.<br/>                                          |
| PrintJobsCollection<br/> | Um conjunto de trabalhos de impressão.<br/>                                                   |
| PrintQueue<br/>          | Imprimir fila em um spooler de impressora.<br/>                                      |
| Serviço<br/>             | Aplicativo em execução como um serviço.<br/>                                      |
| FileService<br/>         | Serviços que acessam o sistema de arquivos.<br/>                                        |
| FileShare<br/>           | Ponto de compartilhamento de arquivo.<br/>                                                      |
| Recurso<br/>            | Um recurso no serviço.<br/>                                             |
| Sessão<br/>             | Uma conexão de serviço de arquivo ativa.<br/>                                     |
| Usuário<br/>                | Conta de usuário local.<br/>                                                    |
| Agrupar<br/>               | Grupo local.<br/>                                                           |
| Usercollection<br/>      | Coleção de usuários locais.<br/>                                             |
| Groupcollection<br/>     | Coleção de grupos locais.<br/>                                            |
| Esquema<br/>              | Contêiner de esquema do WinNT.<br/>                                                |
| Classe<br/>               | Definição de classe de esquema.<br/>                                               |
| Propriedade<br/>            | Definição de atributo de esquema.<br/>                                           |
| Syntax<br/>              | Sintaxe de uma propriedade.<br/>                                                  |



 

 

 





