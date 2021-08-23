---
description: O Instalador grava os seguintes valores no log quando uma ação retorna esses códigos de erro. Para ver toda a lista de códigos de erro retornados pela função Windows Installer MsiExec.exe e InstMsi.exe, consulte Códigos de erro.
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: Registro em log de valores de retorno de ação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 756fa633ef486c3dae4b689acf439f8dbf7786c20f740fb4784de30e764dc9fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945891"
---
# <a name="logging-of-action-return-values"></a>Registro em log de valores de retorno de ação

O Instalador grava os seguintes valores no log quando uma ação retorna esses códigos de erro. Para ver toda a lista de códigos de erro retornados pela função Windows instalador MsiExec.exe e InstMsi.exe, consulte [Códigos de erro](error-codes.md).



| Código do Erro                       | Valores retornados por chamadas de função MsiExec.exe e InstMsi.exe | Valores que aparecem no Log. | Descrição                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FUNÇÃO \_ ERROR \_ NÃO \_ CHAMADA     | 1626                                                           | 0                              | Não foi possível executar uma função.                                                                                                                                                                                                                                               |
| ÊXITO \_ DO ERRO                   | 0                                                              | 1                              | Uma ação foi concluída com êxito.                                                                                                                                                                                                                                               |
| ERRO \_ AO \_ INSTALAR USEREXIT         | 1602                                                           | 2                              | Uma instalação cancelada pelo usuário.                                                                                                                                                                                                                                                   |
| ERRO \_ AO INSTALAR \_ FALHA          | 1603                                                           | 3                              | Um erro fatal.                                                                                                                                                                                                                                                                  |
| ERRO AO \_ INSTALAR \_ SUSPEND          | 1604                                                           | 4                              | A instalação foi suspensa, incompleta.                                                                                                                                                                                                                                         |
| ÊXITO \_ DO ERRO                   | 0                                                              | 5                              | A ação foi concluída com êxito.                                                                                                                                                                                                                                              |
| ERRO \_ ESTADO DE ALÇA \_ \_ INVÁLIDO    | 1609                                                           | 6                              | O handle está em um estado inválido.                                                                                                                                                                                                                                              |
| ERRO \_ DADOS \_ INVÁLIDOS             | 1626                                                           | 7                              | Os dados são inválidos.                                                                                                                                                                                                                                                            |
| ERRO AO \_ INSTALAR \_ JÁ EM \_ EXECUÇÃO | 1618                                                           | 8                              | Outra instalação está em progresso. Somente uma instalação por vez pode executar ações nas tabelas [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence.](advtexecutesequence-table.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Registro em log do instalador](windows-installer-logging.md)
</dt> </dl>

 

 



