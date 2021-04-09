---
title: Método Disable da classe SystemRestore
description: Desabilita o monitoramento em uma unidade específica.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Desabilitar a restauração do sistema de métodos
- Desabilitar a restauração do sistema de método, classe SystemRestore
- Método SystemRestore de restauração do sistema de classe, desabilitar
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085683"
---
# <a name="disable-method-of-the-systemrestore-class"></a><span data-ttu-id="9a000-106">Método Disable da classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="9a000-106">Disable method of the SystemRestore class</span></span>

<span data-ttu-id="9a000-107">Desabilita o monitoramento em uma unidade específica.</span><span class="sxs-lookup"><span data-stu-id="9a000-107">Disables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a000-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a000-108">Syntax</span></span>


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="9a000-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a000-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a000-110">*Unidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a000-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a000-111">A unidade a ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="9a000-111">The drive to be disabled.</span></span> <span data-ttu-id="9a000-112">A cadeia de caracteres da unidade deve estar no formato "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="9a000-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="9a000-113">Se esse parâmetro for a unidade do sistema ou uma cadeia de caracteres vazia (""), nenhuma unidade será monitorada.</span><span class="sxs-lookup"><span data-stu-id="9a000-113">If this parameter is the system drive or an empty string (""), no drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a000-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a000-114">Return value</span></span>

<span data-ttu-id="9a000-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9a000-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9a000-116">Caso contrário, o método retorna um dos códigos de erro COM definidos em WinError. h.</span><span class="sxs-lookup"><span data-stu-id="9a000-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="9a000-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a000-117">Examples</span></span>


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="9a000-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a000-118">Requirements</span></span>



| <span data-ttu-id="9a000-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a000-119">Requirement</span></span> | <span data-ttu-id="9a000-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9a000-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9a000-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a000-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9a000-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9a000-122">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9a000-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a000-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9a000-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9a000-124">None supported</span></span><br/>                                                         |
| <span data-ttu-id="9a000-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="9a000-125">Namespace</span></span><br/>                | <span data-ttu-id="9a000-126">\\Padrão raiz</span><span class="sxs-lookup"><span data-stu-id="9a000-126">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="9a000-127">MOF</span><span class="sxs-lookup"><span data-stu-id="9a000-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a000-128"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a000-128"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a000-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a000-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a000-130">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="9a000-130">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





