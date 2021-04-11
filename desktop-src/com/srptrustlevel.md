---
title: SRPTrustLevel
description: Define o nível de confiança da política de restrição de software (SRP) para aplicativos.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- COM valor do registro SRPTrustLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363837"
---
# <a name="srptrustlevel"></a><span data-ttu-id="436e7-104">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="436e7-104">SRPTrustLevel</span></span>

<span data-ttu-id="436e7-105">Define o nível de confiança da política de restrição de software (SRP) para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="436e7-105">Sets the software restriction policy (SRP) trust level for applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="436e7-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="436e7-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a><span data-ttu-id="436e7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="436e7-107">Remarks</span></span>

<span data-ttu-id="436e7-108">Esse é um valor **reg \_ DWORD** que está disponível a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="436e7-108">This is a **REG\_DWORD** value that is available starting with Windows XP.</span></span>



| <span data-ttu-id="436e7-109">Valor</span><span class="sxs-lookup"><span data-stu-id="436e7-109">Value</span></span>                                 | <span data-ttu-id="436e7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="436e7-110">Description</span></span>                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="436e7-111">0x0 (nível de segurança do cofre não \_ \_ permitido)</span><span class="sxs-lookup"><span data-stu-id="436e7-111">0x0 (SAFER\_LEVELID\_DISALLOWED)</span></span>      | <span data-ttu-id="436e7-112">O aplicativo não é permitido de acessar e de privilégios de usuário sensíveis à segurança.</span><span class="sxs-lookup"><span data-stu-id="436e7-112">The application is disallowed from accessing and security-sensitive user privileges.</span></span> |
| <span data-ttu-id="436e7-113">0x40000 ( \_ nível de \_ FULLYTRUSTED seguro)</span><span class="sxs-lookup"><span data-stu-id="436e7-113">0x40000 (SAFE\_LEVELID\_FULLYTRUSTED)</span></span> | <span data-ttu-id="436e7-114">O aplicativo tem acesso irrestrito aos privilégios do usuário.</span><span class="sxs-lookup"><span data-stu-id="436e7-114">The application has unrestricted access to the user's privileges.</span></span>                    |



 

<span data-ttu-id="436e7-115">Se o valor de **SRPTrustLevel** não existir, \_ será usado o valor padrão de restarid de nível mais seguro \_ .</span><span class="sxs-lookup"><span data-stu-id="436e7-115">If the **SRPTrustLevel** value does not exist, the default value of SAFER\_LEVELID\_DISALLOWED is used.</span></span> <span data-ttu-id="436e7-116">Se **SRPTrustLevel** for do tipo incorreto ou fora do intervalo, com retornará o erro COMAdmin \_ E \_ SAFERINVALID.</span><span class="sxs-lookup"><span data-stu-id="436e7-116">If **SRPTrustLevel** is of the wrong type or out of range, COM returns the error COMADMIN\_E\_SAFERINVALID.</span></span> <span data-ttu-id="436e7-117">Se uma ativação de qualquer classificação falhar devido a verificações de confiança do SRP, COM retornará o erro CO \_ E \_ ACTIVATIONFAILED.</span><span class="sxs-lookup"><span data-stu-id="436e7-117">If an activation of any sort fails because of SRP trust checks, COM returns the error CO\_E\_ACTIVATIONFAILED.</span></span>

## <a name="related-topics"></a><span data-ttu-id="436e7-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="436e7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="436e7-119">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="436e7-119">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="436e7-120">**SRPActivateAsActivatorChecks**</span><span class="sxs-lookup"><span data-stu-id="436e7-120">**SRPActivateAsActivatorChecks**</span></span>](srpactivateasactivatorchecks.md)
</dt> <dt>

[<span data-ttu-id="436e7-121">**SRPRunningObjectChecks**</span><span class="sxs-lookup"><span data-stu-id="436e7-121">**SRPRunningObjectChecks**</span></span>](srprunningobjectchecks.md)
</dt> </dl>

 

 




