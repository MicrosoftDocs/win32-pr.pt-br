---
description: Especificando o protocolo de autenticação
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Especificando o protocolo de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c4688894543a45f49c4af470658da97e30a159c47025398ac7c7ae5e0620e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610506"
---
# <a name="specifying-the-authentication-protocol"></a>Especificando o protocolo de autenticação

Dependendo dos requisitos de segurança em seu site, você pode exigir que o serviço de componentes na fila sempre verifique a identidade de um cliente, nunca para verificar a identidade de um cliente ou para verificar a identidade de um cliente somente se o componente estiver configurado para exigir autenticação mesmo quando não for acessado por meio de uma fila.

> [!Note]  
> Para usar um componente na fila no modo de grupo de trabalho, o nível de autenticação deve ser definido como nenhum.

 

## <a name="component-services-administrative-tool"></a>Ferramenta Administrativa dos Serviços de Componentes

Para especificar o protocolo de autenticação, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em Serviços de Componentes, abra a pasta Aplicativos **COM+** associada ao computador que você deseja gerenciar.

2.  Clique com o botão direito do mouse no aplicativo na fila para o qual você deseja especificar o protocolo de autenticação e clique em **Propriedades**.

3.  Selecione a **guia Ensuamento** na caixa de diálogo propriedades.

4.  Em **Autenticação de Mensagem MSMQ**, selecione o botão de opção associado ao protocolo de autenticação que você deseja implementar.

5.  Clique em **OK**.

## <a name="visual-basic"></a>Visual Basic

Use o *parâmetro AuthLevel* ao ativar o aplicativo na fila, conforme descrito em [Usando o Moniker de Fila.](using-the-queue-moniker.md)

## <a name="cc"></a>C/C++

Use o *parâmetro AuthLevel* ao ativar o aplicativo na fila, conforme descrito em [Usando o Moniker de Fila.](using-the-queue-moniker.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança de componentes na fila](queued-components-security.md)
</dt> <dt>

[Limitações de segurança no modo de grupo de trabalho](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



