---
description: O provedor Microsoft Base Cryptographic é o provedor de CSP (provedor de serviços de criptografia) inicial e é distribuído com as versões 1,0 e 2,0 do CryptoAPI. É um provedor de uso geral que dá suporte a assinaturas digitais e criptografia de dados.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Provedor criptográfico base da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc48060305337dd878dedcadca8cfed52bd2f34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796374"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="371d9-104">Provedor criptográfico base da Microsoft</span><span class="sxs-lookup"><span data-stu-id="371d9-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="371d9-105">O provedor Microsoft Base Cryptographic é o provedor de CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) inicial e é distribuído com as versões 1,0 e 2,0 do [*CryptoAPI*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="371d9-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="371d9-106">É um provedor de uso geral que dá suporte a [*assinaturas digitais*](../secgloss/d-gly.md) e criptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="371d9-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="371d9-107">O algoritmo de chave pública RSA é usado para todas as operações de chave pública.</span><span class="sxs-lookup"><span data-stu-id="371d9-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="371d9-108">Para manter a compatibilidade com versões anteriores, a nova versão do provedor retém a designação da versão 1,0 do nome em Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="371d9-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="371d9-109">No entanto, a versão 2,0 deste provedor está sendo fornecida no momento.</span><span class="sxs-lookup"><span data-stu-id="371d9-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="371d9-110">Para determinar a versão real do provedor em uso, chame [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com o argumento *DwParam* definido como **PP \_ version**.</span><span class="sxs-lookup"><span data-stu-id="371d9-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="371d9-111">Se 0x0200 for retornado em *pbData*, você terá a versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="371d9-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                |                     |
|----------------|---------------------|
| <span data-ttu-id="371d9-112">Tipo de provedor:</span><span class="sxs-lookup"><span data-stu-id="371d9-112">Provider type:</span></span> | <span data-ttu-id="371d9-113">**PROV \_ RSA \_ completo**</span><span class="sxs-lookup"><span data-stu-id="371d9-113">**PROV\_RSA\_FULL**</span></span> |
| <span data-ttu-id="371d9-114">Nome do provedor:</span><span class="sxs-lookup"><span data-stu-id="371d9-114">Provider name:</span></span> | <span data-ttu-id="371d9-115">**Prov de MS \_ Def \_**</span><span class="sxs-lookup"><span data-stu-id="371d9-115">**MS\_DEF\_PROV**</span></span>   |



 

 

 
