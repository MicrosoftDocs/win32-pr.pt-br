---
description: Às vezes, é necessário substituir uma DLL por uma versão mais recente.
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Dynamic-Link atualizações da biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f294e16efac60da843c14d200aaa768d4fc78ce8a922cb0aa6958756a9903be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075536"
---
# <a name="dynamic-link-library-updates"></a>Dynamic-Link atualizações da biblioteca

Às vezes, é necessário substituir uma DLL por uma versão mais recente. Antes de substituir uma DLL, execute uma verificação de versão para garantir que você está substituindo uma versão mais antiga por uma versão mais recente. É possível substituir uma DLL que está em uso. O método usado para substituir DLLs que estão em uso depende do sistema operacional que você está usando. no Windows XP e posterior, os aplicativos devem usar [aplicativos isolados e Assemblies](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)lado a lado.

Não é necessário reiniciar o computador se você executar as seguintes etapas:

1.  Use a função [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) para renomear a DLL que está sendo substituída. Não especifique a cópia MOVEfile \_ \_ permitida e verifique se o arquivo renomeado está no mesmo volume que contém o arquivo original. Você também pode simplesmente renomear o arquivo no mesmo diretório, dando a ele uma extensão diferente.
2.  Copie a nova DLL para o diretório que contém a DLL renomeada. Todos os aplicativos agora usarão a nova DLL.
3.  Use [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) com atraso de MoveFile \_ \_ até \_ a reinicialização para excluir a dll renomeada.

Antes de fazer essa substituição, os aplicativos usarão a DLL original até que ela seja descarregada. Depois de fazer a substituição, os aplicativos usarão a nova DLL. Ao escrever uma DLL, você deve ter cuidado para garantir que ela esteja preparada para essa situação, especialmente se a DLL mantiver informações de estado global ou se comunicar com outros serviços. Se a DLL não estiver preparada para uma alteração nas informações de estado global ou protocolos de comunicação, a atualização da DLL exigirá que você reinicie o computador para garantir que todos os aplicativos estejam usando a mesma versão da DLL.

 

 
