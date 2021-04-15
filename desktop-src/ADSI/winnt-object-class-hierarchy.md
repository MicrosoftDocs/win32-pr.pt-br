---
title: Hierarquia de classe de objeto WinNT
description: A hierarquia da classe de objeto WinNT começa com o objeto namespace.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- ADSI do provedor de serviços WinNT, hierarquia de classe de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498598"
---
# <a name="winnt-object-class-hierarchy"></a>Hierarquia de classe de objeto WinNT

A hierarquia da classe de objeto WinNT começa com o objeto namespace.



| Classe Object                   | Descrição                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| Namespace<br/>           | Contêiner de objeto de nível superior.<br/>                                            |
| Domínio<br/>              | O domínio do Windows NT.<br/>                                                 |
| Usuário<br/>                | Conta de usuário.<br/>                                                          |
| Agrupar<br/>               | Conta de grupo para gerenciar direitos de acesso.<br/>                              |
| Usergroupcollection<br/> | Um conjunto de grupos de usuários implementando [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/>  |
| GroupCollection<br/>     | Um conjunto de outros grupos que implementam [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/> |
| Computador<br/>            | Servidor ou estação de trabalho do Windows NT 4,0.<br/>                                  |
| PrintJob<br/>            | Trabalho de impressão na fila de impressão.<br/>                                          |
| Trabalhos de trabalho<br/> | Um conjunto de trabalhos de impressão.<br/>                                                   |
| PrintQueue<br/>          | Fila de impressão em um spooler de impressora.<br/>                                      |
| Serviço<br/>             | Aplicativo em execução como um serviço.<br/>                                      |
| FileService<br/>         | Serviços acessando o sistema de arquivos.<br/>                                        |
| FileShare<br/>           | Ponto de compartilhamento de arquivos.<br/>                                                      |
| Recurso<br/>            | Um recurso no serviço.<br/>                                             |
| Session<br/>             | Uma conexão de serviço de arquivo ativo.<br/>                                     |
| Usuário<br/>                | Conta de usuário local.<br/>                                                    |
| Agrupar<br/>               | Grupo local.<br/>                                                           |
| UserCollection<br/>      | Coleção de usuários locais.<br/>                                             |
| GroupCollection<br/>     | Coleção de grupos locais.<br/>                                            |
| Esquema<br/>              | Contêiner de esquema WinNT.<br/>                                                |
| Classe<br/>               | Definição de classe de esquema.<br/>                                               |
| Propriedade<br/>            | Definição de atributo de esquema.<br/>                                           |
| Syntax<br/>              | Sintaxe de uma propriedade.<br/>                                                  |



 

 

 





