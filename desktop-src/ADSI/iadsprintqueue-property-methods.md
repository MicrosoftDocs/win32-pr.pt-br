---
title: Métodos de propriedade IADsPrintQueue (IADs. h)
description: Os métodos de propriedade da interface IADsPrintQueue obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 7f5b4200-65c8-4230-8561-ad4fefb391f3
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPrintQueue
topic_type:
- apiref
api_name:
- IADsPrintQueue Property Methods
- IADsPrintQueue.BannerPage
- IADsPrintQueue.get_BannerPage
- IADsPrintQueue.put_BannerPage
- IADsPrintQueue.Datatype
- IADsPrintQueue.get_Datatype
- IADsPrintQueue.put_Datatype
- IADsPrintQueue.DefaultJobPriority
- IADsPrintQueue.get_DefaultJobPriority
- IADsPrintQueue.put_DefaultJobPriority
- IADsPrintQueue.Description
- IADsPrintQueue.get_Description
- IADsPrintQueue.put_Description
- IADsPrintQueue.HostComputer
- IADsPrintQueue.get_HostComputer
- IADsPrintQueue.put_HostComputer
- IADsPrintQueue.Location
- IADsPrintQueue.get_Location
- IADsPrintQueue.put_Location
- IADsPrintQueue.Model
- IADsPrintQueue.get_Model
- IADsPrintQueue.put_Model
- IADsPrintQueue.PrintDevices
- IADsPrintQueue.get_PrintDevices
- IADsPrintQueue.put_PrintDevices
- IADsPrintQueue.PrinterPath
- IADsPrintQueue.get_PrinterPath
- IADsPrintQueue.put_PrinterPath
- IADsPrintQueue.PrintProcessor
- IADsPrintQueue.get_PrintProcessor
- IADsPrintQueue.put_PrintProcessor
- IADsPrintQueue.Priority
- IADsPrintQueue.get_Priority
- IADsPrintQueue.put_Priority
- IADsPrintQueue.StartTime
- IADsPrintQueue.get_StartTime
- IADsPrintQueue.put_StartTime
- IADsPrintQueue.UntilTime
- IADsPrintQueue.get_UntilTime
- IADsPrintQueue.put_UntilTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e8b7b2260805dbf5fa144f239111b6e29f5ec78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163604"
---
# <a name="iadsprintqueue-property-methods"></a><span data-ttu-id="4e27d-105">Métodos de propriedade IADsPrintQueue</span><span class="sxs-lookup"><span data-stu-id="4e27d-105">IADsPrintQueue Property Methods</span></span>

<span data-ttu-id="4e27d-106">Os métodos de propriedade da interface [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4e27d-106">The property methods of the [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="4e27d-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4e27d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4e27d-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4e27d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4e27d-109">**BannerPage**</span><span class="sxs-lookup"><span data-stu-id="4e27d-109">**BannerPage**</span></span>
<span data-ttu-id="4e27d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-111">O caminho do sistema de arquivos que aponta para a página de faixa usada para separar trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="4e27d-111">The file system path that points to the banner page used to separate print jobs.</span></span> <span data-ttu-id="4e27d-112">Se for **NULL**, nenhuma página de faixa será usada.</span><span class="sxs-lookup"><span data-stu-id="4e27d-112">If **NULL**, no banner page is used.</span></span>

<dt>

<span data-ttu-id="4e27d-113">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-114">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4e27d-114">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BannerPage(
  [out] BSTR* pbstrBannerPage
);
HRESULT put_BannerPage(
  [in] BSTR bstrBannerPage
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-115">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4e27d-115">**Datatype**</span></span>
<span data-ttu-id="4e27d-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-117">O tipo de dados que pode ser processado por essa fila.</span><span class="sxs-lookup"><span data-stu-id="4e27d-117">The data type that can be processed by this queue.</span></span>

<dt>

<span data-ttu-id="4e27d-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-119">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4e27d-119">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Datatype(
  [out] BSTR* pbstrDatatype
);
HRESULT put_Datatype(
  [in] BSTR bstrDatatype
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-120">**DefaultJobPriority**</span><span class="sxs-lookup"><span data-stu-id="4e27d-120">**DefaultJobPriority**</span></span>
<span data-ttu-id="4e27d-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-122">A prioridade padrão atribuída a cada trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="4e27d-122">The default priority assigned to each print job.</span></span>

<dt>

<span data-ttu-id="4e27d-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-124">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4e27d-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultJobPriority(
  [out] LONG* plDefaultJobPriority
);
HRESULT put_DefaultJobPriority(
  [in] BSTR lDefaultJobPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4e27d-125">**Description**</span></span>
<span data-ttu-id="4e27d-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-127">A descrição de texto desta fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="4e27d-127">The text description of this print queue.</span></span>

<dt>

<span data-ttu-id="4e27d-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-129">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4e27d-129">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-130">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="4e27d-130">**HostComputer**</span></span>
<span data-ttu-id="4e27d-131"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-131"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-132">A cadeia de caracteres ADsPath que faz referência ao computador host.</span><span class="sxs-lookup"><span data-stu-id="4e27d-132">The ADsPath string that references the host computer.</span></span>

<dt>

<span data-ttu-id="4e27d-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-134">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4e27d-134">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-135">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="4e27d-135">**Location**</span></span>
<span data-ttu-id="4e27d-136"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-136"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-137">O local da fila, conforme descrito por um administrador.</span><span class="sxs-lookup"><span data-stu-id="4e27d-137">The location of the queue as described by an administrator.</span></span>

<dt>

<span data-ttu-id="4e27d-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-139">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4e27d-139">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-140">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="4e27d-140">**Model**</span></span>
<span data-ttu-id="4e27d-141"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-141"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-142">O nome do driver usado por esta fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="4e27d-142">The name of the driver used by this print queue.</span></span>

<dt>

<span data-ttu-id="4e27d-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-144">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4e27d-144">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-145">**Dispositivos de redispositivo**</span><span class="sxs-lookup"><span data-stu-id="4e27d-145">**PrintDevices**</span></span>
<span data-ttu-id="4e27d-146"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-146"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-147">Um SAFEARRAY de **BSTR** que contém os nomes dos dispositivos de impressão para os quais essa fila de impressão coloca trabalhos em spool.</span><span class="sxs-lookup"><span data-stu-id="4e27d-147">A SAFEARRAY of **BSTR** that contains the names of the print devices to which this print queue spools jobs.</span></span>

<dt>

<span data-ttu-id="4e27d-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-149">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4e27d-149">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintDevices(
  [out] VARIANT* pvPrintDevices
);
HRESULT put_PrintDevices(
  [in] VARIANT vPrintDevices
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-150">**PrinterPath**</span><span class="sxs-lookup"><span data-stu-id="4e27d-150">**PrinterPath**</span></span>
<span data-ttu-id="4e27d-151"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-151"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-152">A cadeia de caracteres que faz referência ao caminho pelo qual uma impressora compartilhada pode ser acessada.</span><span class="sxs-lookup"><span data-stu-id="4e27d-152">The string that references the path by which a shared printer can be accessed.</span></span>

<dt>

<span data-ttu-id="4e27d-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-154">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4e27d-154">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrinterPath(
  [out] BSTR* pbstrPrinterPath
);
HRESULT put_PrinterPath(
  [in] BSTR bstrPrinterPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-155">**Multiprocessador**</span><span class="sxs-lookup"><span data-stu-id="4e27d-155">**PrintProcessor**</span></span>
<span data-ttu-id="4e27d-156"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-156"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-157">O processador de impressão associado a esta fila.</span><span class="sxs-lookup"><span data-stu-id="4e27d-157">The print processor associated with this queue.</span></span>

<dt>

<span data-ttu-id="4e27d-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-159">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4e27d-159">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintProcessor(
  [out] BSTR* pbstrPrintProcessor
);
HRESULT put_PrintProcessor(
  [in] BSTR bstrPrintProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-160">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="4e27d-160">**Priority**</span></span>
<span data-ttu-id="4e27d-161"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-161"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-162">A prioridade dessa fila de trabalhos de objeto de impressora para todos os dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="4e27d-162">The priority of this printer object job queue for any connected devices.</span></span> <span data-ttu-id="4e27d-163">Todos os trabalhos em objetos da fila de impressão de prioridade mais alta serão processados primeiro.</span><span class="sxs-lookup"><span data-stu-id="4e27d-163">All jobs in higher priority print queue objects will be processed first.</span></span>

<dt>

<span data-ttu-id="4e27d-164">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-164">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-165">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="4e27d-165">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Priority(
  [out] LONG* plPriority
);
HRESULT put_Priority(
  [in] LONG lPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-166">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4e27d-166">**StartTime**</span></span>
<span data-ttu-id="4e27d-167"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-167"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-168">A hora em que a fila deve começar a processar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="4e27d-168">The time when the queue should begin processing jobs.</span></span> <span data-ttu-id="4e27d-169">A parte de data da hora é ignorada.</span><span class="sxs-lookup"><span data-stu-id="4e27d-169">The date portion of the time is ignored.</span></span>

<dt>

<span data-ttu-id="4e27d-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-171">Tipo de dados de script: **Data**</span><span class="sxs-lookup"><span data-stu-id="4e27d-171">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartTime(
  [out] DATE* pdateStartTime
);
HRESULT put_StartTime(
  [in] DATE dateStartTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e27d-172">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="4e27d-172">**UntilTime**</span></span>
<span data-ttu-id="4e27d-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4e27d-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="4e27d-174">A hora em que a fila deve parar de processar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="4e27d-174">The time when the queue should stop processing jobs.</span></span>

<dt>

<span data-ttu-id="4e27d-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4e27d-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e27d-176">Tipo de dados de script: **Data**</span><span class="sxs-lookup"><span data-stu-id="4e27d-176">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
HRESULT put_UntilTime(
  [in] DATE dateUntilTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="4e27d-177">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e27d-177">Examples</span></span>

<span data-ttu-id="4e27d-178">O exemplo de código a seguir mostra como determinar se uma impressora especificada está online ou offline.</span><span class="sxs-lookup"><span data-stu-id="4e27d-178">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```VB
Dim pq As IADsPrintQueue
Dim pqo As IADsPrintQueueOperations
On Error GoTo Cleanup
 
Set pq = GetObject("WinNT://aMachine/aPrinter")
Set pqo = pq
If pqo.status = ADS_PRINTER_OFFLINE Then
    MsgBox pq.Model & "@" & pq.Location & is offline."
Else
    MsgBox pq.Model & "@" & pq.Location & is online."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pq = Nothing
    Set pqo = Nothing
```



<span data-ttu-id="4e27d-179">O exemplo de código a seguir mostra como determinar se uma impressora especificada está online ou offline.</span><span class="sxs-lookup"><span data-stu-id="4e27d-179">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```C++
IADsPrintQueue *pq = NULL;
HRESULT hr = S_OK;
IADsPrintQueueOperations *pqo = NULL;
BSTR model = NULL;
BSTR location = NULL;

LPWSTR adsPath = L"WinNT://aMachine/aPrinter";
hr = ADsGetObject(adsPath,
                  IID_IADsPrintQueue,
                  (void**)&pq);
if(FAILED(hr)) {goto Cleanup;}


hr = pq->QueryInterface(IID_IADsPrintQueueOperations,(void**)&pqo);
if(FAILED(hr)) {goto Cleanup;}

long status;
hr = pqo->get_Status(&status);
if(FAILED(hr)) {goto Cleanup;}

hr = pq->get_Model(&model);
if(FAILED(hr)) {goto Cleanup;}

hr =pq->get_Location(&location);
if(FAILED(hr)) {goto Cleanup;}

if(status == ADS_PRINTER_OFFLINE) 
{
    printf("%S @ %S is offline.\n",model,location);
} 
else 
{
    printf("%S @ %S is online.\n",model,location);
}


Cleanup:
    SysFreeString(model);
    SysFreeString(location);
    if(pq) pq->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="4e27d-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e27d-180">Requirements</span></span>



| <span data-ttu-id="4e27d-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e27d-181">Requirement</span></span> | <span data-ttu-id="4e27d-182">Valor</span><span class="sxs-lookup"><span data-stu-id="4e27d-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e27d-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e27d-183">Minimum supported client</span></span><br/> | <span data-ttu-id="4e27d-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e27d-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e27d-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e27d-185">Minimum supported server</span></span><br/> | <span data-ttu-id="4e27d-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e27d-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e27d-187">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e27d-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e27d-188"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e27d-188"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4e27d-189">DLL</span><span class="sxs-lookup"><span data-stu-id="4e27d-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e27d-190"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e27d-190"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4e27d-191">IID</span><span class="sxs-lookup"><span data-stu-id="4e27d-191">IID</span></span><br/>                      | <span data-ttu-id="4e27d-192">IID \_ IADsPrintQueue é definido como B15160D0-1226-11CF-A985-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="4e27d-192">IID\_IADsPrintQueue is defined as B15160D0-1226-11CF-A985-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4e27d-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e27d-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e27d-194">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="4e27d-194">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="4e27d-195">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="4e27d-195">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





