---
title: Mapeando sintaxe de Active Directory para sintaxe ADSI
description: A tabela a seguir mapeia as sintaxes de Active Directory para suas sintaxes ADSI correspondentes.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- atributos ADSI, mapeando Active Directory sintaxe para sintaxe ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754417"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a><span data-ttu-id="c12dd-104">Mapeando sintaxe de Active Directory para sintaxe ADSI</span><span class="sxs-lookup"><span data-stu-id="c12dd-104">Mapping Active Directory Syntax to ADSI Syntax</span></span>

<span data-ttu-id="c12dd-105">A tabela a seguir mapeia as sintaxes de Active Directory para suas sintaxes ADSI correspondentes.</span><span class="sxs-lookup"><span data-stu-id="c12dd-105">The following table maps the Active Directory syntaxes to their corresponding ADSI syntaxes.</span></span>



| <span data-ttu-id="c12dd-106">ID da sintaxe do atributo</span><span class="sxs-lookup"><span data-stu-id="c12dd-106">Attribute syntax ID</span></span> | <span data-ttu-id="c12dd-107">Tipo de sintaxe Active Directory</span><span class="sxs-lookup"><span data-stu-id="c12dd-107">Active Directory syntax type</span></span>             | <span data-ttu-id="c12dd-108">Tipo de sintaxe ADSI equivalente</span><span class="sxs-lookup"><span data-stu-id="c12dd-108">Equivalent ADSI syntax type</span></span>                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c12dd-109">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="c12dd-109">2.5.5.1</span></span><br/>  | <span data-ttu-id="c12dd-110">Cadeia de caracteres DN</span><span class="sxs-lookup"><span data-stu-id="c12dd-110">DN String</span></span><br/>                     | <span data-ttu-id="c12dd-111">Cadeia de caracteres DN</span><span class="sxs-lookup"><span data-stu-id="c12dd-111">DN String</span></span><br/>                                                |
| <span data-ttu-id="c12dd-112">2.5.5.2</span><span class="sxs-lookup"><span data-stu-id="c12dd-112">2.5.5.2</span></span><br/>  | <span data-ttu-id="c12dd-113">ID de objeto</span><span class="sxs-lookup"><span data-stu-id="c12dd-113">Object ID</span></span><br/>                     | <span data-ttu-id="c12dd-114">Cadeia de caracteres CaseIgnore</span><span class="sxs-lookup"><span data-stu-id="c12dd-114">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="c12dd-115">2.5.5.3</span><span class="sxs-lookup"><span data-stu-id="c12dd-115">2.5.5.3</span></span><br/>  | <span data-ttu-id="c12dd-116">Cadeia de caracteres diferencia maiúsculas de minúscula</span><span class="sxs-lookup"><span data-stu-id="c12dd-116">Case Sensitive String</span></span><br/>         | <span data-ttu-id="c12dd-117">Cadeia de caracteres CaseExact</span><span class="sxs-lookup"><span data-stu-id="c12dd-117">CaseExact String</span></span><br/>                                         |
| <span data-ttu-id="c12dd-118">2.5.5.4</span><span class="sxs-lookup"><span data-stu-id="c12dd-118">2.5.5.4</span></span><br/>  | <span data-ttu-id="c12dd-119">Cadeia de caracteres ignorada de caso</span><span class="sxs-lookup"><span data-stu-id="c12dd-119">Case Ignored String</span></span><br/>           | <span data-ttu-id="c12dd-120">Cadeia de caracteres CaseIgnore</span><span class="sxs-lookup"><span data-stu-id="c12dd-120">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="c12dd-121">2.5.5.5</span><span class="sxs-lookup"><span data-stu-id="c12dd-121">2.5.5.5</span></span><br/>  | <span data-ttu-id="c12dd-122">Imprimir cadeia de caracteres de caso</span><span class="sxs-lookup"><span data-stu-id="c12dd-122">Print Case String</span></span><br/>             | <span data-ttu-id="c12dd-123">Cadeia de caracteres imprimível</span><span class="sxs-lookup"><span data-stu-id="c12dd-123">Printable String</span></span><br/>                                         |
| <span data-ttu-id="c12dd-124">2.5.5.6</span><span class="sxs-lookup"><span data-stu-id="c12dd-124">2.5.5.6</span></span><br/>  | <span data-ttu-id="c12dd-125">Cadeia de caracteres numérica</span><span class="sxs-lookup"><span data-stu-id="c12dd-125">Numeric String</span></span><br/>                | <span data-ttu-id="c12dd-126">Cadeia de caracteres numérica</span><span class="sxs-lookup"><span data-stu-id="c12dd-126">Numeric String</span></span><br/>                                           |
| <span data-ttu-id="c12dd-127">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="c12dd-127">2.5.5.7</span></span><br/>  | <span data-ttu-id="c12dd-128">**Ou** Nome DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="c12dd-128">**OR** Name DNWithOctetString</span></span><br/> | <span data-ttu-id="c12dd-129">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="c12dd-129">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="c12dd-130">2.5.5.8</span><span class="sxs-lookup"><span data-stu-id="c12dd-130">2.5.5.8</span></span><br/>  | <span data-ttu-id="c12dd-131">Booliano</span><span class="sxs-lookup"><span data-stu-id="c12dd-131">Boolean</span></span><br/>                       | <span data-ttu-id="c12dd-132">Booliano</span><span class="sxs-lookup"><span data-stu-id="c12dd-132">Boolean</span></span><br/>                                                  |
| <span data-ttu-id="c12dd-133">2.5.5.9</span><span class="sxs-lookup"><span data-stu-id="c12dd-133">2.5.5.9</span></span><br/>  | <span data-ttu-id="c12dd-134">Integer</span><span class="sxs-lookup"><span data-stu-id="c12dd-134">Integer</span></span><br/>                       | <span data-ttu-id="c12dd-135">Integer</span><span class="sxs-lookup"><span data-stu-id="c12dd-135">Integer</span></span><br/>                                                  |
| <span data-ttu-id="c12dd-136">2.5.5.10</span><span class="sxs-lookup"><span data-stu-id="c12dd-136">2.5.5.10</span></span><br/> | <span data-ttu-id="c12dd-137">Cadeia de caracteres de octeto</span><span class="sxs-lookup"><span data-stu-id="c12dd-137">Octet String</span></span><br/>                  | <span data-ttu-id="c12dd-138">Cadeia de caracteres de octeto</span><span class="sxs-lookup"><span data-stu-id="c12dd-138">Octet String</span></span><br/>                                             |
| <span data-ttu-id="c12dd-139">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="c12dd-139">2.5.5.11</span></span><br/> | <span data-ttu-id="c12dd-140">Hora</span><span class="sxs-lookup"><span data-stu-id="c12dd-140">Time</span></span><br/>                          | <span data-ttu-id="c12dd-141">Hora UTC</span><span class="sxs-lookup"><span data-stu-id="c12dd-141">UTC Time</span></span><br/>                                                 |
| <span data-ttu-id="c12dd-142">2.5.5.12</span><span class="sxs-lookup"><span data-stu-id="c12dd-142">2.5.5.12</span></span><br/> | <span data-ttu-id="c12dd-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="c12dd-143">Unicode</span></span><br/>                       | <span data-ttu-id="c12dd-144">Cadeia de caracteres de Ignorar maiúsculas</span><span class="sxs-lookup"><span data-stu-id="c12dd-144">Case Ignore String</span></span><br/>                                       |
| <span data-ttu-id="c12dd-145">2.5.5.13</span><span class="sxs-lookup"><span data-stu-id="c12dd-145">2.5.5.13</span></span><br/> | <span data-ttu-id="c12dd-146">Endereço</span><span class="sxs-lookup"><span data-stu-id="c12dd-146">Address</span></span><br/>                       | <span data-ttu-id="c12dd-147">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="c12dd-147">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="c12dd-148">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="c12dd-148">2.5.5.14</span></span><br/> | <span data-ttu-id="c12dd-149">Distname-Address</span><span class="sxs-lookup"><span data-stu-id="c12dd-149">Distname-Address</span></span><br/>              |                                                                     |
| <span data-ttu-id="c12dd-150">2.5.5.15</span><span class="sxs-lookup"><span data-stu-id="c12dd-150">2.5.5.15</span></span><br/> | <span data-ttu-id="c12dd-151">Descritor de segurança NT</span><span class="sxs-lookup"><span data-stu-id="c12dd-151">NT Security Descriptor</span></span><br/>        | [<span data-ttu-id="c12dd-152">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c12dd-152">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| <span data-ttu-id="c12dd-153">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="c12dd-153">2.5.5.16</span></span><br/> | <span data-ttu-id="c12dd-154">Inteiro grande</span><span class="sxs-lookup"><span data-stu-id="c12dd-154">Large Integer</span></span><br/>                 | [<span data-ttu-id="c12dd-155">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="c12dd-155">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| <span data-ttu-id="c12dd-156">2.5.5.17</span><span class="sxs-lookup"><span data-stu-id="c12dd-156">2.5.5.17</span></span><br/> | <span data-ttu-id="c12dd-157">SID</span><span class="sxs-lookup"><span data-stu-id="c12dd-157">SID</span></span><br/>                           | <span data-ttu-id="c12dd-158">Cadeia de caracteres de octeto</span><span class="sxs-lookup"><span data-stu-id="c12dd-158">Octet String</span></span><br/>                                             |



 

 

 





