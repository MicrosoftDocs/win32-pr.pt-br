---
description: Desliga o thread de resolução de nomes de usuário.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Método DiskQuotaControl. ShutdownNameResolution (Dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010442"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a><span data-ttu-id="f57cd-103">Método DiskQuotaControl. ShutdownNameResolution</span><span class="sxs-lookup"><span data-stu-id="f57cd-103">DiskQuotaControl.ShutdownNameResolution method</span></span>

<span data-ttu-id="f57cd-104">Desliga o thread de resolução de nomes de usuário.</span><span class="sxs-lookup"><span data-stu-id="f57cd-104">Shuts down the user name resolution thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="f57cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f57cd-105">Syntax</span></span>


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a><span data-ttu-id="f57cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f57cd-106">Parameters</span></span>

<span data-ttu-id="f57cd-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f57cd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f57cd-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f57cd-108">Return value</span></span>

<span data-ttu-id="f57cd-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f57cd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f57cd-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f57cd-110">Remarks</span></span>

<span data-ttu-id="f57cd-111">O resolvedor de nome de SID (identificador de segurança) traduz o SID para nomes de usuário em um thread em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f57cd-111">The security identifier (SID) name resolver translates SID to user names on a background thread.</span></span> <span data-ttu-id="f57cd-112">Esse thread é desligado automaticamente quando o objeto de controle de cota associado é destruído.</span><span class="sxs-lookup"><span data-stu-id="f57cd-112">This thread is shut down automatically when the associated quota control object is destroyed.</span></span> <span data-ttu-id="f57cd-113">No entanto, há alguns casos em que o thread não é mais necessário, mas o objeto ainda não está pronto para ser destruído.</span><span class="sxs-lookup"><span data-stu-id="f57cd-113">However, there are some cases when the thread is no longer needed, but the object is not yet ready to be destroyed.</span></span> <span data-ttu-id="f57cd-114">Um exemplo típico é quando nenhum processamento adicional está ocorrendo, mas os clientes ainda estão mantendo referências ao objeto.</span><span class="sxs-lookup"><span data-stu-id="f57cd-114">A typical example is when no further processing is taking place, but clients are still holding references to the object.</span></span> <span data-ttu-id="f57cd-115">O método **ShutdownNameResolution** permite encerrar o thread do resolvedor e liberar os recursos associados sem destruir o objeto de controle de cota.</span><span class="sxs-lookup"><span data-stu-id="f57cd-115">The **ShutdownNameResolution** method allows you to terminate the resolver thread and free the associated resources without destroying the quota control object.</span></span>

> [!Note]  
> <span data-ttu-id="f57cd-116">Quando você desligar o thread do resolvedor, a resolução de nomes assíncronas será interrompida imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f57cd-116">When you shut down the resolver thread, asynchronous name resolution immediately stops.</span></span> <span data-ttu-id="f57cd-117">Se as chamadas forem feitas posteriormente para métodos como [**adduser**](diskquotacontrol-adduser.md) ou [**FindUser**](diskquotacontrol-finduser.md), o objeto de cota poderá recriar o thread do resolvedor.</span><span class="sxs-lookup"><span data-stu-id="f57cd-117">If calls are subsequently made to methods such as [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md), the quota object might re-create the resolver thread.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f57cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f57cd-118">Requirements</span></span>



| <span data-ttu-id="f57cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f57cd-119">Requirement</span></span> | <span data-ttu-id="f57cd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f57cd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f57cd-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f57cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f57cd-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f57cd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f57cd-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f57cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f57cd-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f57cd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f57cd-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f57cd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f57cd-126"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="f57cd-126"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="f57cd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f57cd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f57cd-128"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f57cd-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f57cd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f57cd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f57cd-130">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="f57cd-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




