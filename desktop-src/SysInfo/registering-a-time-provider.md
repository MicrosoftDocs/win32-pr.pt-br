---
description: O sistema carrega um provedor de tempo com base em suas informações de configuração armazenadas no registro.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrando um provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828683"
---
# <a name="registering-a-time-provider"></a><span data-ttu-id="5a8a2-103">Registrando um provedor de tempo</span><span class="sxs-lookup"><span data-stu-id="5a8a2-103">Registering a Time Provider</span></span>

<span data-ttu-id="5a8a2-104">O sistema carrega um provedor de tempo com base em suas informações de configuração armazenadas no registro.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-104">The system loads a time provider based on its configuration information stored in the registry.</span></span> <span data-ttu-id="5a8a2-105">Cada provedor de tempo deve criar a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="5a8a2-105">Each time provider should create the following registry key:</span></span>

<span data-ttu-id="5a8a2-106">**HKEY \_ \_ \\ Sistema de máquina local** \\ **CurrentControlSet** \\ **Serviços** \\ **W32Time** \\ **timefornecedores** \\ *ProviderName*</span><span class="sxs-lookup"><span data-stu-id="5a8a2-106">**HKEY\_LOCAL\_MACHINE\\System**\\**CurrentControlSet**\\**Services**\\**W32Time**\\**TimeProviders**\\*ProviderName*</span></span>

<span data-ttu-id="5a8a2-107">A tabela a seguir descreve os valores que devem existir na chave de cada provedor.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-107">The following table describes the values that must exist in each provider's key.</span></span>



| <span data-ttu-id="5a8a2-108">Valor</span><span class="sxs-lookup"><span data-stu-id="5a8a2-108">Value</span></span>             | <span data-ttu-id="5a8a2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a8a2-109">Description</span></span>                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8a2-110">**DllName**</span><span class="sxs-lookup"><span data-stu-id="5a8a2-110">**DllName**</span></span>       | <span data-ttu-id="5a8a2-111">O nome da DLL que contém o provedor.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-111">The name of the DLL that contains the provider.</span></span> <span data-ttu-id="5a8a2-112">Esse valor tem o tipo **reg \_ sz**.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-112">This value has the type **REG\_SZ**.</span></span>                                                                                                                                     |
| <span data-ttu-id="5a8a2-113">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="5a8a2-113">**Enabled**</span></span>       | <span data-ttu-id="5a8a2-114">Indica se o provedor deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-114">Indicates whether the provider should be started.</span></span> <span data-ttu-id="5a8a2-115">Se esse valor for 1, o provedor será iniciado.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-115">If this value is 1, the provider is started.</span></span> <span data-ttu-id="5a8a2-116">Caso contrário, o provedor não será iniciado.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-116">Otherwise, the provider is not started.</span></span> <span data-ttu-id="5a8a2-117">Esse valor tem o tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-117">This value has the type **REG\_DWORD**.</span></span>                                           |
| <span data-ttu-id="5a8a2-118">**InputProvider**</span><span class="sxs-lookup"><span data-stu-id="5a8a2-118">**InputProvider**</span></span> | <span data-ttu-id="5a8a2-119">Indica se o provedor é um provedor de entrada ou um provedor de saída.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-119">Indicates whether the provider is an input provider or an output provider.</span></span> <span data-ttu-id="5a8a2-120">Se esse valor for 1, o provedor será um provedor de entrada.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-120">If this value is 1, the provider is an input provider.</span></span> <span data-ttu-id="5a8a2-121">Caso contrário, o provedor será um provedor de saída.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-121">Otherwise, the provider is an output provider.</span></span> <span data-ttu-id="5a8a2-122">Esse valor tem o tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-122">This value has the type **REG\_DWORD**.</span></span> |



 

<span data-ttu-id="5a8a2-123">O Gerenciador de provedores de tempo enumera as chaves sob a chave **Timefornecedores** e inicia cada provedor habilitado.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-123">The time provider manager enumerates the keys under the **TimeProviders** key and starts each enabled provider.</span></span> <span data-ttu-id="5a8a2-124">Os provedores são iniciados na inicialização do sistema e sempre que há alterações de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-124">Providers are started at system startup and whenever there are parameter changes.</span></span>

<span data-ttu-id="5a8a2-125">Cada provedor de tempo também pode armazenar informações de configuração específicas do aplicativo no registro.</span><span class="sxs-lookup"><span data-stu-id="5a8a2-125">Each time provider can also store application-specific configuration information in the registry.</span></span>

 

 



