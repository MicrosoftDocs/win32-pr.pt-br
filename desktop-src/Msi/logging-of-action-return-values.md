---
description: O instalador grava os seguintes valores no log quando uma ação retorna esses códigos de erro. Para obter a lista completa de códigos de erro retornados pelo Windows Installer chamadas de função MsiExec.exe e InstMsi.exe, consulte códigos de erro.
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: Registro de valores de retorno de ação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaaa203fee1fbb02bef070d065a9838383ea588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810324"
---
# <a name="logging-of-action-return-values"></a>Registro de valores de retorno de ação

O instalador grava os seguintes valores no log quando uma ação retorna esses códigos de erro. Para obter a lista completa de códigos de erro retornados pelo Windows Installer chamadas de função MsiExec.exe e InstMsi.exe, consulte [códigos de erro](error-codes.md).



| Código de erro                       | Valores retornados por chamadas de função MsiExec.exe e InstMsi.exe | Valores que aparecem no log. | Descrição                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| função de erro \_ \_ não \_ chamada     | 1626                                                           | 0                              | Não foi possível executar uma função.                                                                                                                                                                                                                                               |
| êxito do erro \_                   | 0                                                              | 1                              | Uma ação foi concluída com êxito.                                                                                                                                                                                                                                               |
| ERRO ao \_ instalar o \_ UserExit         | 1602                                                           | 2                              | Um usuário cancelou A instalação.                                                                                                                                                                                                                                                   |
| \_falha na instalação do erro \_          | 1603                                                           | 3                              | Um erro fatal.                                                                                                                                                                                                                                                                  |
| ERRO ao \_ instalar \_ suspensão          | 1604                                                           | 4                              | A instalação foi suspensa, incompleta.                                                                                                                                                                                                                                         |
| êxito do erro \_                   | 0                                                              | 5                              | A ação foi concluída com êxito.                                                                                                                                                                                                                                              |
| ERRO \_ de \_ identificador de \_ estado inválido    | 1609                                                           | 6                              | O identificador está em um estado inválido.                                                                                                                                                                                                                                              |
| ERRO de \_ dados inválidos \_             | 1626                                                           | 7                              | Os dados são inválidos.                                                                                                                                                                                                                                                            |
| ERRO de \_ instalação \_ já \_ em execução | 1618                                                           | 8                              | Outra instalação está em progresso. Somente uma instalação por vez pode executar ações nas tabelas [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence](advtexecutesequence-table.md) . |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Log de Windows Installer](windows-installer-logging.md)
</dt> </dl>

 

 



