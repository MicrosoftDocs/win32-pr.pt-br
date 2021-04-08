---
title: Métodos de propriedade IADsPrintJobOperations (IADs. h)
description: Os métodos de propriedade da interface IADsPrintJobOperations lêem e gravam as propriedades listadas na tabela a seguir. Para obter mais informações sobre métodos de propriedade, consulte interface Property Methods.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPrintJobOperations
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2981fcdd8043c0eb0ee8b05cfd0331fe3abfabe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824628"
---
# <a name="iadsprintjoboperations-property-methods"></a><span data-ttu-id="8f2e2-105">Métodos de propriedade IADsPrintJobOperations</span><span class="sxs-lookup"><span data-stu-id="8f2e2-105">IADsPrintJobOperations Property Methods</span></span>

<span data-ttu-id="8f2e2-106">Os métodos de propriedade da interface [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) lêem e gravam as propriedades listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-106">The property methods of the [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) interface read and write the properties listed in the following table.</span></span> <span data-ttu-id="8f2e2-107">Para obter mais informações sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8f2e2-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8f2e2-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f2e2-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="8f2e2-109">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-109">**PagesPrinted**</span></span>
<span data-ttu-id="8f2e2-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8f2e2-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="8f2e2-111">Contém o número de páginas impressas.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-111">Contains the number of pages printed.</span></span>

<dt>

<span data-ttu-id="8f2e2-112">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f2e2-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f2e2-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8f2e2-114">**Posição**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-114">**Position**</span></span>
<span data-ttu-id="8f2e2-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8f2e2-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="8f2e2-116">Contém a posição desse trabalho de impressão na fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-116">Contains the position of this print job in the print queue.</span></span>

<dt>

<span data-ttu-id="8f2e2-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8f2e2-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f2e2-118">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8f2e2-119">**Status**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-119">**Status**</span></span>
<span data-ttu-id="8f2e2-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8f2e2-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="8f2e2-121">Contém o status atual do trabalho de impressão, conforme indicado por um dos valores [**constantes de status do trabalho de impressão ADSI**](adsi-print-job-status-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="8f2e2-121">Contains the current status of the print job as indicated by one of the [**ADSI Print Job Status Constants**](adsi-print-job-status-constants.md) values.</span></span>

<dt>

<span data-ttu-id="8f2e2-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f2e2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f2e2-123">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8f2e2-124">**Tempo decorrido**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-124">**TimeElapsed**</span></span>
<span data-ttu-id="8f2e2-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8f2e2-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="8f2e2-126">Contém o número de milissegundos decorridos desde o início do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-126">Contains the number of milliseconds elapsed since the print job started.</span></span>

<dt>

<span data-ttu-id="8f2e2-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f2e2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f2e2-128">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="8f2e2-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f2e2-129">Examples</span></span>

<span data-ttu-id="8f2e2-130">O exemplo de código a seguir mostra como as propriedades de [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-130">The following code example shows how the properties for [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) may be used.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a><span data-ttu-id="8f2e2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f2e2-131">Requirements</span></span>



| <span data-ttu-id="8f2e2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f2e2-132">Requirement</span></span> | <span data-ttu-id="8f2e2-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8f2e2-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2e2-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f2e2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8f2e2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f2e2-135">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="8f2e2-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f2e2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8f2e2-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f2e2-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="8f2e2-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f2e2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f2e2-139"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f2e2-139"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="8f2e2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8f2e2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f2e2-141"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f2e2-141"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="8f2e2-142">IID</span><span class="sxs-lookup"><span data-stu-id="8f2e2-142">IID</span></span><br/>                      | <span data-ttu-id="8f2e2-143">IID \_ IADsPrintJobOperations é definido como 32FB6780-1ED0-11CF-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="8f2e2-143">IID\_IADsPrintJobOperations is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f2e2-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f2e2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f2e2-145">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-145">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="8f2e2-146">**IADsPrintJobOperations**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-146">**IADsPrintJobOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[<span data-ttu-id="8f2e2-147">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-147">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="8f2e2-148">**Constantes de status do trabalho de impressão ADSI**</span><span class="sxs-lookup"><span data-stu-id="8f2e2-148">**ADSI Print Job Status Constants**</span></span>](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





