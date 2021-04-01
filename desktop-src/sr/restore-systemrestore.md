---
title: Método Restore da classe SystemRestore
description: Inicia uma restauração do sistema.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restaurar restauração do sistema do método
- Restaurar método restauração do sistema, classe SystemRestore
- Restauração do sistema de classe SystemRestore, método Restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644352"
---
# <a name="restore-method-of-the-systemrestore-class"></a><span data-ttu-id="5eab6-106">Método Restore da classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="5eab6-106">Restore method of the SystemRestore class</span></span>

<span data-ttu-id="5eab6-107">Inicia uma restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="5eab6-107">Initiates a system restore.</span></span> <span data-ttu-id="5eab6-108">O chamador deve forçar a reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="5eab6-108">The caller must force a system reboot.</span></span> <span data-ttu-id="5eab6-109">A restauração real ocorre durante a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="5eab6-109">The actual restoration occurs during the reboot.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eab6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5eab6-110">Syntax</span></span>


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="5eab6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5eab6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eab6-112">*SequenceNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5eab6-112">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eab6-113">O número de sequência do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="5eab6-113">The sequence number of the restore point.</span></span> <span data-ttu-id="5eab6-114">Para determinar o número de sequência de um ponto de restauração específico, enumere todos os pontos de restauração no sistema.</span><span class="sxs-lookup"><span data-stu-id="5eab6-114">To determine the sequence number for a specific restore point, enumerate all restore points on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eab6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5eab6-115">Return value</span></span>

<span data-ttu-id="5eab6-116">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5eab6-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5eab6-117">Caso contrário, o método retorna um dos códigos de erro COM definidos em WinError. h.</span><span class="sxs-lookup"><span data-stu-id="5eab6-117">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="5eab6-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5eab6-118">Examples</span></span>


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a><span data-ttu-id="5eab6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eab6-119">Requirements</span></span>



| <span data-ttu-id="5eab6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eab6-120">Requirement</span></span> | <span data-ttu-id="5eab6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5eab6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5eab6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5eab6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5eab6-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5eab6-123">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5eab6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5eab6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5eab6-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5eab6-125">None supported</span></span><br/>                                                         |
| <span data-ttu-id="5eab6-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="5eab6-126">Namespace</span></span><br/>                | <span data-ttu-id="5eab6-127">\\ \\ Padrão raiz</span><span class="sxs-lookup"><span data-stu-id="5eab6-127">Root\\\\Default</span></span><br/>                                                        |
| <span data-ttu-id="5eab6-128">MOF</span><span class="sxs-lookup"><span data-stu-id="5eab6-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5eab6-129"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5eab6-129"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eab6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5eab6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eab6-131">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="5eab6-131">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





