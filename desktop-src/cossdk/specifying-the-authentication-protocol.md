---
description: Especificando o protocolo de autenticação
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Especificando o protocolo de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457050"
---
# <a name="specifying-the-authentication-protocol"></a>Especificando o protocolo de autenticação

Dependendo dos requisitos de segurança no seu site, você pode exigir que o serviço de componentes na fila sempre verifique a identidade do cliente, nunca para verificar a identidade de um cliente ou para verificar a identidade de um cliente somente se o componente estiver configurado para exigir autenticação mesmo quando não for acessado por meio de uma fila.

> [!Note]  
> Para usar um componente enfileirado no modo de grupo de trabalho, o nível de autenticação deve ser definido como nenhum.

 

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Para especificar o protocolo de autenticação, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.

2.  Clique com o botão direito do mouse no aplicativo em fila para o qual você deseja especificar o protocolo de autenticação e clique em **Propriedades**.

3.  Selecione a guia **enfileiramento** na caixa de diálogo Propriedades.

4.  Em **autenticação de mensagens MSMQ**, selecione o botão de opção associado ao protocolo de autenticação que você deseja implementar.

5.  Clique em **OK**.

## <a name="visual-basic"></a>Visual Basic

Use o parâmetro *AuthLevel* ao ativar o aplicativo enfileirado conforme descrito no [moniker usando a fila](using-the-queue-moniker.md).

## <a name="cc"></a>C/C++

Use o parâmetro *AuthLevel* ao ativar o aplicativo enfileirado conforme descrito no [moniker usando a fila](using-the-queue-moniker.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança de componentes na fila](queued-components-security.md)
</dt> <dt>

[Limitações de segurança no modo de grupo de trabalho](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



