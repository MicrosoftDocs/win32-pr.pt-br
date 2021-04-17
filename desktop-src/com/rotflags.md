---
title: ROTFlags
description: Controla o registro de um servidor COM na corrompidos (tabela de objetos em execução).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- COM valor do registro ROTFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813712"
---
# <a name="rotflags"></a><span data-ttu-id="6a107-104">ROTFlags</span><span class="sxs-lookup"><span data-stu-id="6a107-104">ROTFlags</span></span>

<span data-ttu-id="6a107-105">Controla o registro de um servidor COM na corrompidos (tabela de objetos em execução).</span><span class="sxs-lookup"><span data-stu-id="6a107-105">Controls the registration of a COM server in the running object table (ROT).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6a107-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="6a107-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a><span data-ttu-id="6a107-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a107-107">Remarks</span></span>

<span data-ttu-id="6a107-108">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6a107-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="6a107-109">Valor de sinalizador</span><span class="sxs-lookup"><span data-stu-id="6a107-109">Flag Value</span></span> | <span data-ttu-id="6a107-110">Constante</span><span class="sxs-lookup"><span data-stu-id="6a107-110">Constant</span></span>                        |
|------------|---------------------------------|
| <span data-ttu-id="6a107-111">0x1</span><span class="sxs-lookup"><span data-stu-id="6a107-111">0x1</span></span>        | <span data-ttu-id="6a107-112">**ROTREGFLAGS \_ ALLOWANYCLIENT**</span><span class="sxs-lookup"><span data-stu-id="6a107-112">**ROTREGFLAGS\_ALLOWANYCLIENT**</span></span> |



 

### <a name="rotregflags_allowanyclient-description"></a><span data-ttu-id="6a107-113">Descrição do ROTREGFLAGS \_ ALLOWANYCLIENT</span><span class="sxs-lookup"><span data-stu-id="6a107-113">ROTREGFLAGS\_ALLOWANYCLIENT Description</span></span>

<span data-ttu-id="6a107-114">Se um servidor COM quiser se registrar no corrompidos e permitir que qualquer cliente acesse o registro, ele deverá usar o sinalizador **ROTFLAGS \_ ALLOWANYCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="6a107-114">If a COM server wants to register in the ROT and allow any client to access the registration, it must use the **ROTFLAGS\_ALLOWANYCLIENT** flag.</span></span> <span data-ttu-id="6a107-115">Um servidor COM "Activate as Activator" não pode especificar **ROTFLAGS \_ ALLOWANYCLIENT** porque o DCOMSCM (Gerenciador de controle de serviço) do DCOM impõe uma verificação de falsificação nesse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6a107-115">An "Activate As Activator" COM server cannot specify **ROTFLAGS\_ALLOWANYCLIENT** because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="6a107-116">Portanto, no Windows Vista e posterior, o COM adiciona suporte para a entrada de registro **ROTFlags** que permite ao servidor estipular que seus registros corrompidos são disponibilizados para qualquer cliente.</span><span class="sxs-lookup"><span data-stu-id="6a107-116">Therefore, in Windows Vista and later, COM adds support for the **ROTFlags** registry entry that allows the server to stipulate that its ROT registrations be made available to any client.</span></span>

<span data-ttu-id="6a107-117">A entrada deve existir no hive **do \_ \_ computador local hKey** .</span><span class="sxs-lookup"><span data-stu-id="6a107-117">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span> <span data-ttu-id="6a107-118">Essa entrada fornece um servidor "Activate as Activator" com a mesma funcionalidade que o **ROTFLAGS \_ ALLOWANYCLIENT** fornece para um servidor runas.</span><span class="sxs-lookup"><span data-stu-id="6a107-118">This entry provides an "Activate As Activator" server with the same functionality that **ROTFLAGS\_ALLOWANYCLIENT** provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a107-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a107-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a107-120">Chave AppID</span><span class="sxs-lookup"><span data-stu-id="6a107-120">AppID Key</span></span>](appid-key.md)
</dt> <dt>

[<span data-ttu-id="6a107-121">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="6a107-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="6a107-122">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="6a107-122">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




