---
title: InvalidSecurityDescriptorLoggingLevel
description: Define o detalhamento das entradas do log de eventos sobre descritores de segurança inválidos para permissões de acesso e de inicialização do componente.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- COM valor do registro InvalidSecurityDescriptorLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291759"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a><span data-ttu-id="dc23d-104">InvalidSecurityDescriptorLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="dc23d-104">InvalidSecurityDescriptorLoggingLevel</span></span>

<span data-ttu-id="dc23d-105">Define o detalhamento das entradas do log de eventos sobre descritores de segurança inválidos para permissões de acesso e de inicialização do componente.</span><span class="sxs-lookup"><span data-stu-id="dc23d-105">Sets the verbosity of event log entries about invalid security descriptors for component launch and access permissions.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="dc23d-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="dc23d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="dc23d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc23d-107">Remarks</span></span>

<span data-ttu-id="dc23d-108">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="dc23d-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="dc23d-109">Valor</span><span class="sxs-lookup"><span data-stu-id="dc23d-109">Value</span></span> | <span data-ttu-id="dc23d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc23d-110">Description</span></span>                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc23d-111">1</span><span class="sxs-lookup"><span data-stu-id="dc23d-111">1</span></span>     | <span data-ttu-id="dc23d-112">Sempre Registre falhas quando o COM encontrar um descritor de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="dc23d-112">Always log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="dc23d-113">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="dc23d-113">This is the default value.</span></span>                                                                                  |
| <span data-ttu-id="dc23d-114">2</span><span class="sxs-lookup"><span data-stu-id="dc23d-114">2</span></span>     | <span data-ttu-id="dc23d-115">Nunca Registre falhas quando o COM encontrar um descritor de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="dc23d-115">Never log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="dc23d-116">Não é recomendável desabilitar o log de eventos, pois isso pode dificultar o diagnóstico de problemas.</span><span class="sxs-lookup"><span data-stu-id="dc23d-116">It is not recommended that you disable event logging, as it can make it more difficult to diagnose problems.</span></span> |



 

<span data-ttu-id="dc23d-117">Se você definir os descritores de segurança de permissão de acesso e inicialização (comumente chamados de ACLs) diretamente, será possível construir um descritor de segurança cujo significado não possa ser interpretado sem ambigüidade.</span><span class="sxs-lookup"><span data-stu-id="dc23d-117">If you set launch and access permission security descriptors (commonly called ACLs) directly, it is possible to construct a security descriptor whose meaning cannot be interpreted unambiguously.</span></span> <span data-ttu-id="dc23d-118">COM faz uma entrada no log de eventos quando ele encontra um descritor de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="dc23d-118">COM makes an event log entry when it encounters such an invalid security descriptor.</span></span>

<span data-ttu-id="dc23d-119">Observe que [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) e [**CallFailureLoggingLevel**](callfailurelogginglevel.md) não têm controle sobre o log de erros de descritor de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="dc23d-119">Note that [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) and [**CallFailureLoggingLevel**](callfailurelogginglevel.md) have no control over logging invalid security descriptor errors.</span></span> <span data-ttu-id="dc23d-120">Use **InvalidSecurityDescriptorLoggingLevel** para ter controle total sobre essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="dc23d-120">Use **InvalidSecurityDescriptorLoggingLevel** for full control over this functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc23d-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc23d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc23d-122">Definindo a segurança para aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="dc23d-122">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




