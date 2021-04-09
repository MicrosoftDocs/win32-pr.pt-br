---
title: OverrideEAPCertificateSelection
description: A chave do registro OverrideEAPCertificateSelection determina se o cliente substituirá o comportamento de seleção de certificado de cartão inteligente padrão e fornecerá a ele mais certificados para sua escolha.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103823488"
---
# <a name="overrideeapcertificateselection"></a><span data-ttu-id="3e8cc-103">OverrideEAPCertificateSelection</span><span class="sxs-lookup"><span data-stu-id="3e8cc-103">OverrideEAPCertificateSelection</span></span>

<span data-ttu-id="3e8cc-104">A chave do registro OverrideEAPCertificateSelection determina se o cliente substituirá o comportamento de seleção de certificado de cartão inteligente padrão e fornecerá a ele mais certificados para sua escolha.</span><span class="sxs-lookup"><span data-stu-id="3e8cc-104">The OverrideEAPCertificateSelection registry key determines whether the client will override the default smart card certificate selection behavior and provide the user with more certificates to choose from.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3e8cc-105">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="3e8cc-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a><span data-ttu-id="3e8cc-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e8cc-106">Remarks</span></span>

<span data-ttu-id="3e8cc-107">Esse é um **valor \_ binário reg** .</span><span class="sxs-lookup"><span data-stu-id="3e8cc-107">This is a **REG\_BINARY** value.</span></span>



| <span data-ttu-id="3e8cc-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3e8cc-108">Value</span></span> | <span data-ttu-id="3e8cc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e8cc-109">Description</span></span>                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8cc-110">0x000</span><span class="sxs-lookup"><span data-stu-id="3e8cc-110">0x000</span></span> | <span data-ttu-id="3e8cc-111">Não substitua o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="3e8cc-111">Do not override the default behavior.</span></span>                                                                                                                                                                |
| <span data-ttu-id="3e8cc-112">0x001</span><span class="sxs-lookup"><span data-stu-id="3e8cc-112">0x001</span></span> | <span data-ttu-id="3e8cc-113">Escolha o último certificado anexado do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="3e8cc-113">Choose the last attached certificate from the smart card.</span></span>                                                                                                                                            |
| <span data-ttu-id="3e8cc-114">0x010</span><span class="sxs-lookup"><span data-stu-id="3e8cc-114">0x010</span></span> | <span data-ttu-id="3e8cc-115">Mostra todos os certificados na interface do usuário de seleção de certificado do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="3e8cc-115">Shows all certificates in the certificate selection UI from the smart card.</span></span>                                                                                                                          |
| <span data-ttu-id="3e8cc-116">0x100</span><span class="sxs-lookup"><span data-stu-id="3e8cc-116">0x100</span></span> | <span data-ttu-id="3e8cc-117">Mostra todos os certificados na interface do usuário de seleção de certificado do registro.</span><span class="sxs-lookup"><span data-stu-id="3e8cc-117">Shows all certificates in the certificate selection UI from the registry.</span></span>                                                                                                                            |
| <span data-ttu-id="3e8cc-118">0x101</span><span class="sxs-lookup"><span data-stu-id="3e8cc-118">0x101</span></span> | <span data-ttu-id="3e8cc-119">Mostra todos os certificados na interface do usuário de seleção de certificado do registro e o último certificado anexado do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="3e8cc-119">Shows all certificates in the certificate selection UI from the registry and the last attached certificate from the smart card.</span></span> <span data-ttu-id="3e8cc-120">Mostra o último certificado anexado do cartão inteligente, conforme selecionado.</span><span class="sxs-lookup"><span data-stu-id="3e8cc-120">Shows the last attached certificate from the smart card as selected.</span></span> |
| <span data-ttu-id="3e8cc-121">0x110</span><span class="sxs-lookup"><span data-stu-id="3e8cc-121">0x110</span></span> | <span data-ttu-id="3e8cc-122">Mostra todos os certificados na interface do usuário de seleção de certificado do registro e do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="3e8cc-122">Shows all certificates in the certificate selection UI from the registry and the smart card.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="3e8cc-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e8cc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e8cc-124">Configurações do registro EAPHost</span><span class="sxs-lookup"><span data-stu-id="3e8cc-124">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




