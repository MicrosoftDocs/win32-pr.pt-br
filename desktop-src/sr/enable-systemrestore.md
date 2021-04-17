---
title: Habilitar o método da classe SystemRestore
description: Habilita o monitoramento em uma unidade específica.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Habilitar restauração do sistema de métodos
- Habilitar a restauração do sistema de método, classe SystemRestore
- Restauração do sistema de classe SystemRestore, método Enable
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790349"
---
# <a name="enable-method-of-the-systemrestore-class"></a><span data-ttu-id="a5f61-106">Habilitar o método da classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="a5f61-106">Enable method of the SystemRestore class</span></span>

<span data-ttu-id="a5f61-107">Habilita o monitoramento em uma unidade específica.</span><span class="sxs-lookup"><span data-stu-id="a5f61-107">Enables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f61-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5f61-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="a5f61-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5f61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f61-110">*Unidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5f61-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f61-111">A unidade a ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="a5f61-111">The drive to be enabled.</span></span> <span data-ttu-id="a5f61-112">A cadeia de caracteres da unidade deve estar no formato "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="a5f61-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="a5f61-113">Se esse parâmetro for a unidade do sistema ou uma cadeia de caracteres vazia (""), todas as unidades serão monitoradas.</span><span class="sxs-lookup"><span data-stu-id="a5f61-113">If this parameter is the system drive or an empty string (""), all drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f61-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5f61-114">Return value</span></span>

<span data-ttu-id="a5f61-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a5f61-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a5f61-116">Caso contrário, o método retorna um dos códigos de erro COM definidos em WinError. h.</span><span class="sxs-lookup"><span data-stu-id="a5f61-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f61-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5f61-117">Remarks</span></span>

<span data-ttu-id="a5f61-118">O método **Enable** não aguarda o monitoramento ser totalmente habilitado antes de ser retornado, pois isso pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="a5f61-118">The **Enable** method does not wait for monitoring to be enabled completely before it returns, because this could take a while.</span></span> <span data-ttu-id="a5f61-119">Em vez disso, ele retorna imediatamente após iniciar o serviço de restauração do sistema e o driver de filtro.</span><span class="sxs-lookup"><span data-stu-id="a5f61-119">Instead, it returns immediately after starting the System Restore service and filter driver.</span></span>

<span data-ttu-id="a5f61-120">Para habilitar a restauração do sistema em uma unidade que não seja do sistema, você deve primeiro habilitar a restauração do sistema na unidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="a5f61-120">To enable System Restore on a non-system drive, you must first enable System Restore on the system drive.</span></span>

<span data-ttu-id="a5f61-121">Esse método falha no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="a5f61-121">This method fails in safe mode.</span></span>

## <a name="examples"></a><span data-ttu-id="a5f61-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5f61-122">Examples</span></span>


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="a5f61-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5f61-123">Requirements</span></span>



| <span data-ttu-id="a5f61-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5f61-124">Requirement</span></span> | <span data-ttu-id="a5f61-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a5f61-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a5f61-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5f61-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a5f61-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a5f61-127">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a5f61-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5f61-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a5f61-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a5f61-129">None supported</span></span><br/>                                                         |
| <span data-ttu-id="a5f61-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5f61-130">Namespace</span></span><br/>                | <span data-ttu-id="a5f61-131">\\Padrão raiz</span><span class="sxs-lookup"><span data-stu-id="a5f61-131">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="a5f61-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a5f61-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5f61-133"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5f61-133"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5f61-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5f61-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f61-135">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="a5f61-135">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





