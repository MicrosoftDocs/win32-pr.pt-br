---
description: Windows O instalador executa as seguintes ações durante a reinstalação de um aplicativo quando o pacote contém componentes isolados. Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Reinstalação de componentes isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c624777647ab9e5023cd6c78d9aaa4d20951563f915afcd800ba60ca3b233174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086006"
---
# <a name="reinstallation-of-isolated-components"></a>Reinstalação de componentes isolados

Windows O instalador executa as seguintes ações durante a reinstalação de um aplicativo quando o pacote contém componentes isolados. Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.

## <a name="reinstallation"></a>Reinstalação

-   Reinstale os arquivos do componente \_ compartilhado na mesma pasta que o aplicativo de componente \_ somente se o aplicativo de componente \_ também estiver sendo reinstalado.
-   Não incrementar a lista de componentes compartilhados do cliente \_ e não incrementar a contagem de SharedDLL.
-   Recrie o arquivo de byte zero com o nome de arquivo curto do arquivo de chave do \_ aplicativo de componente. Esse arquivo deve estar localizado na mesma pasta que \_ o aplicativo de componente e ter a extensão. LOCAL.
-   Reinstale todos os recursos do aplicativo de componente \_ como de costume.

Se o Refcount SharedDLL para o componente \_ compartilhado for maior que 1, ou se outros produtos permanecerem na lista de componentes \_ compartilhados do cliente:

-   Reinstale nenhum arquivo no local compartilhado do componente \_ compartilhado.

Se o Refcount SharedDLL para o componente \_ compartilhado for igual a 1 ou se não houver nenhum outro cliente restante do componente \_ compartilhado:

-   Reinstale os arquivos do componente \_ compartilhado no local compartilhado usando as [regras de controle de versão de arquivo](file-versioning-rules.md).
-   Processar todas as ações de reinstalação para componente \_ compartilhado.
-   Se o componente \_ compartilhado for um componente com, registre o caminho com completo, de modo que as sintaxes do instalador \[ $Component \] e \[ \# FileKey \] apontem para o local compartilhado do componente \_ compartilhado.

 

 



