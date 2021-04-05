---
title: Métodos de propriedade IADsPrintQueueOperations (IADs. h)
description: Os métodos de propriedade da interface IADsPrintQueueOperations lêem e gravam as propriedades listadas na lista a seguir. Para obter mais informações sobre métodos de propriedade, consulte interface Property Methods.
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPrintQueueOperations
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8af7aef94dd9453af690f0c5d83b1e978d3b058
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918885"
---
# <a name="iadsprintqueueoperations-property-methods"></a><span data-ttu-id="42cd5-105">Métodos de propriedade IADsPrintQueueOperations</span><span class="sxs-lookup"><span data-stu-id="42cd5-105">IADsPrintQueueOperations Property Methods</span></span>

<span data-ttu-id="42cd5-106">Os métodos de propriedade da interface [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) lêem e gravam as propriedades listadas na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="42cd5-106">The property methods of the [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) interface read and write the properties listed in the following list.</span></span> <span data-ttu-id="42cd5-107">Para obter mais informações sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="42cd5-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="42cd5-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="42cd5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="42cd5-109">**Status**</span><span class="sxs-lookup"><span data-stu-id="42cd5-109">**Status**</span></span>
<span data-ttu-id="42cd5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="42cd5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="42cd5-111">Status atual das operações da fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="42cd5-111">Current status of the print queue operations.</span></span> <span data-ttu-id="42cd5-112">Os valores de código de status válidos são listados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="42cd5-112">The valid status code values are listed in the following list.</span></span>

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

<span data-ttu-id="42cd5-113">**Anúncios \_ do IMPRESSORA \_ pausada** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="42cd5-113">**ADS\_PRINTER\_PAUSED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

<span data-ttu-id="42cd5-114">**Anúncios \_ do \_ \_ Exclusão de impressora pendente** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="42cd5-114">**ADS\_PRINTER\_PENDING\_DELETION** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

<span data-ttu-id="42cd5-115">**Anúncios \_ do \_Erro de impressora** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="42cd5-115">**ADS\_PRINTER\_ERROR** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

<span data-ttu-id="42cd5-116">**Anúncios \_ do \_ \_ Obstrução de papel da impressora** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="42cd5-116">**ADS\_PRINTER\_PAPER\_JAM** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

<span data-ttu-id="42cd5-117">**Anúncios \_ do \_Papel de \_ saída da impressora** (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="42cd5-117">**ADS\_PRINTER\_PAPER\_OUT** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

<span data-ttu-id="42cd5-118">**Anúncios \_ do \_ \_ Alimentação manual da impressora** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="42cd5-118">**ADS\_PRINTER\_MANUAL\_FEED** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

<span data-ttu-id="42cd5-119">**Anúncios \_ do \_ \_ Problema de papel da impressora** (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="42cd5-119">**ADS\_PRINTER\_PAPER\_PROBLEM** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

<span data-ttu-id="42cd5-120">**Anúncios \_ do IMPRESSORA \_ offline** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="42cd5-120">**ADS\_PRINTER\_OFFLINE** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

<span data-ttu-id="42cd5-121">**Anúncios \_ do \_E/ \_ s de impressora ativa** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="42cd5-121">**ADS\_PRINTER\_IO\_ACTIVE** (0x00000100)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

<span data-ttu-id="42cd5-122">**Anúncios \_ do IMPRESSORA \_ ocupada** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="42cd5-122">**ADS\_PRINTER\_BUSY** (0x00000200)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

<span data-ttu-id="42cd5-123">**Anúncios \_ do \_Impressão de impressora** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="42cd5-123">**ADS\_PRINTER\_PRINTING** (0x00000400)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

<span data-ttu-id="42cd5-124">**Anúncios \_ do Bandeja de saída de impressora \_ \_ \_ cheia** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="42cd5-124">**ADS\_PRINTER\_OUTPUT\_BIN\_FULL** (0x00000800)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

<span data-ttu-id="42cd5-125">**Anúncios \_ do IMPRESSORA \_ não \_ disponível** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-125">**ADS\_PRINTER\_NOT\_AVAILABLE** (0x00001000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

<span data-ttu-id="42cd5-126">**Anúncios \_ do IMPRESSORA \_ aguardando** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-126">**ADS\_PRINTER\_WAITING** (0x00002000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

<span data-ttu-id="42cd5-127">**Anúncios \_ do \_Processamento de impressora** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-127">**ADS\_PRINTER\_PROCESSING** (0x00004000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

<span data-ttu-id="42cd5-128">**Anúncios \_ do \_Inicialização de impressora** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-128">**ADS\_PRINTER\_INITIALIZING** (0x00008000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

<span data-ttu-id="42cd5-129">**Anúncios \_ do \_Aquecimento da \_ impressora** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-129">**ADS\_PRINTER\_WARMING\_UP** (0x00010000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

<span data-ttu-id="42cd5-130">**Anúncios \_ do \_Toner \_ da impressora baixo** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-130">**ADS\_PRINTER\_TONER\_LOW** (0x00020000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

<span data-ttu-id="42cd5-131">**Anúncios \_ do \_Sem \_ toner da impressora** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-131">**ADS\_PRINTER\_NO\_TONER** (0x00040000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

<span data-ttu-id="42cd5-132">**Anúncios \_ do \_ \_ Apontador de página da impressora** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-132">**ADS\_PRINTER\_PAGE\_PUNT** (0x00080000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

<span data-ttu-id="42cd5-133">**Anúncios \_ do \_ \_ Intervenção do usuário da impressora** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-133">**ADS\_PRINTER\_USER\_INTERVENTION** (0x00100000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

<span data-ttu-id="42cd5-134">**Anúncios \_ do IMPRESSORA \_ sem \_ \_ memória** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-134">**ADS\_PRINTER\_OUT\_OF\_MEMORY** (0x00200000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

<span data-ttu-id="42cd5-135">**Anúncios \_ do Porta de impressora \_ \_ aberta** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-135">**ADS\_PRINTER\_DOOR\_OPEN** (0x00400000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

<span data-ttu-id="42cd5-136">**Anúncios \_ do Servidor de impressora \_ \_ desconhecido** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-136">**ADS\_PRINTER\_SERVER\_UNKNOWN** (0x00800000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

<span data-ttu-id="42cd5-137">**Anúncios \_ do \_ \_ Economia de energia de impressora** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="42cd5-137">**ADS\_PRINTER\_POWER\_SAVE** (0x01000000)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="42cd5-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42cd5-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42cd5-139">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="42cd5-139">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="42cd5-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="42cd5-140">Examples</span></span>

<span data-ttu-id="42cd5-141">O exemplo de código a seguir Visual Basic verifica se uma impressora está emperrada.</span><span class="sxs-lookup"><span data-stu-id="42cd5-141">The following Visual Basic code example verifies that a printer is jammed.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



<span data-ttu-id="42cd5-142">O exemplo de código C++ a seguir verifica se uma impressora está emperrada.</span><span class="sxs-lookup"><span data-stu-id="42cd5-142">The following C++ code example verifies that a printer is jammed.</span></span>


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="42cd5-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42cd5-143">Requirements</span></span>



| <span data-ttu-id="42cd5-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="42cd5-144">Requirement</span></span> | <span data-ttu-id="42cd5-145">Valor</span><span class="sxs-lookup"><span data-stu-id="42cd5-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="42cd5-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42cd5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="42cd5-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42cd5-147">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="42cd5-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42cd5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="42cd5-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42cd5-149">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="42cd5-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42cd5-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="42cd5-151"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="42cd5-151"><dt>Iads.h</dt></span></span> </dl>           |
| <span data-ttu-id="42cd5-152">DLL</span><span class="sxs-lookup"><span data-stu-id="42cd5-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42cd5-153"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42cd5-153"><dt>Activeds.dll</dt></span></span> </dl>     |
| <span data-ttu-id="42cd5-154">IID</span><span class="sxs-lookup"><span data-stu-id="42cd5-154">IID</span></span><br/>                      | <span data-ttu-id="42cd5-155">IID \_ IADsPrintQueueOperations é definido como 124BE5C0-156E-11CF-A986-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="42cd5-155">IID\_IADsPrintQueueOperations is defined as 124BE5C0-156E-11CF-A986-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42cd5-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="42cd5-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42cd5-157">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="42cd5-157">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="42cd5-158">**IADsPrintQueueOperations**</span><span class="sxs-lookup"><span data-stu-id="42cd5-158">**IADsPrintQueueOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





