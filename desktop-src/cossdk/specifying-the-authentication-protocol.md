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
# <a name="specifying-the-authentication-protocol"></a><span data-ttu-id="3435a-103">Especificando o protocolo de autenticação</span><span class="sxs-lookup"><span data-stu-id="3435a-103">Specifying the Authentication Protocol</span></span>

<span data-ttu-id="3435a-104">Dependendo dos requisitos de segurança no seu site, você pode exigir que o serviço de componentes na fila sempre verifique a identidade do cliente, nunca para verificar a identidade de um cliente ou para verificar a identidade de um cliente somente se o componente estiver configurado para exigir autenticação mesmo quando não for acessado por meio de uma fila.</span><span class="sxs-lookup"><span data-stu-id="3435a-104">Depending on the security requirements at your site, you can require the queued components service always to verify a client's identity, never to verify a client's identity, or to verify a client's identity only if the component is configured to require authentication even when not accessed through a queue.</span></span>

> [!Note]  
> <span data-ttu-id="3435a-105">Para usar um componente enfileirado no modo de grupo de trabalho, o nível de autenticação deve ser definido como nenhum.</span><span class="sxs-lookup"><span data-stu-id="3435a-105">In order to use a queued component in workgroup mode, the authentication level must be set to none.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="3435a-106">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="3435a-106">Component Services Administrative Tool</span></span>

<span data-ttu-id="3435a-107">Para especificar o protocolo de autenticação, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3435a-107">To specify the authentication protocol, use the following steps:</span></span>

1.  <span data-ttu-id="3435a-108">Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.</span><span class="sxs-lookup"><span data-stu-id="3435a-108">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="3435a-109">Clique com o botão direito do mouse no aplicativo em fila para o qual você deseja especificar o protocolo de autenticação e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="3435a-109">Right-click the queued application for which you want to specify the authentication protocol, and then click **Properties**.</span></span>

3.  <span data-ttu-id="3435a-110">Selecione a guia **enfileiramento** na caixa de diálogo Propriedades.</span><span class="sxs-lookup"><span data-stu-id="3435a-110">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="3435a-111">Em **autenticação de mensagens MSMQ**, selecione o botão de opção associado ao protocolo de autenticação que você deseja implementar.</span><span class="sxs-lookup"><span data-stu-id="3435a-111">Under **MSMQ Message Authentication**, select the radio button associated with the authentication protocol you want to implement.</span></span>

5.  <span data-ttu-id="3435a-112">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="3435a-112">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3435a-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3435a-113">Visual Basic</span></span>

<span data-ttu-id="3435a-114">Use o parâmetro *AuthLevel* ao ativar o aplicativo enfileirado conforme descrito no [moniker usando a fila](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="3435a-114">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="cc"></a><span data-ttu-id="3435a-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="3435a-115">C/C++</span></span>

<span data-ttu-id="3435a-116">Use o parâmetro *AuthLevel* ao ativar o aplicativo enfileirado conforme descrito no [moniker usando a fila](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="3435a-116">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3435a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3435a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3435a-118">Segurança de componentes na fila</span><span class="sxs-lookup"><span data-stu-id="3435a-118">Queued Components Security</span></span>](queued-components-security.md)
</dt> <dt>

[<span data-ttu-id="3435a-119">Limitações de segurança no modo de grupo de trabalho</span><span class="sxs-lookup"><span data-stu-id="3435a-119">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



