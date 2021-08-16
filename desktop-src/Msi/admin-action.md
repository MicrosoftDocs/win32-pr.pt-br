---
description: A ação de administrador é uma ação de nível superior usada para executar instalações administrativas.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Ação de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785bd69a8de7da1df9a812f7e89d589b6e939b3eedd6b3cecb66bf86407636cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145929"
---
# <a name="admin-action"></a>Ação de administrador

A ação de administrador é uma ação de nível superior usada para executar [instalações administrativas](administrative-installation.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

a ação de administrador não é chamada de dentro da sequência da tabela de ações, Windows Installer executa essa ação quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) é chamado com o parâmetro *szCommandLine* definido como "action = ADMIN" ou o executável de linha de comando Msiexec.exe é chamado com a opção de linha de comando "/a".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Tabela AdminExecuteSequence](adminexecutesequence-table.md)
</dt> </dl>

 

 



