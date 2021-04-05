---
description: Recupera uma variedade de informações para a bateria.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION código de controle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921724"
---
# <a name="ioctl_battery_query_information-control-code"></a><span data-ttu-id="c5ba1-103">\_Código de \_ controle de informações de consulta da bateria do IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="c5ba1-103">IOCTL\_BATTERY\_QUERY\_INFORMATION control code</span></span>

<span data-ttu-id="c5ba1-104">Recupera uma variedade de informações para a bateria.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-104">Retrieves a variety of information for the battery.</span></span>

<span data-ttu-id="c5ba1-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="c5ba1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5ba1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ba1-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="c5ba1-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba1-108">Um identificador para a bateria em que as informações serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-108">A handle to the battery on which information is to be returned.</span></span> <span data-ttu-id="c5ba1-109">Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="c5ba1-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba1-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="c5ba1-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba1-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-111">The control code for the operation.</span></span> <span data-ttu-id="c5ba1-112">Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="c5ba1-113">Use **\_ \_ \_ as informações de consulta da bateria do IOCTL** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-113">Use **IOCTL\_BATTERY\_QUERY\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba1-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="c5ba1-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba1-115">Um ponteiro para uma estrutura de [**\_ \_ informações de consulta de bateria**](battery-query-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ba1-115">A pointer to a [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba1-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="c5ba1-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba1-117">O tamanho do buffer de entrada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba1-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="c5ba1-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba1-119">Um ponteiro para o buffer de retorno.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-119">A pointer to the return buffer.</span></span> <span data-ttu-id="c5ba1-120">O tipo de dados (e, portanto, tamanho) do buffer de retorno depende das informações solicitadas no membro do nível de informações de consulta da bateria da estrutura de [**\_ \_ informações de consulta da bateria**](battery-query-information-str.md) de entrada. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-120">The data type (and, therefore, size) of the return buffer depends on the information requested in the **BATTERY\_QUERY\_INFORMATION\_LEVEL** member of the input [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

<span data-ttu-id="c5ba1-121">A tabela a seguir mostra os dados retornados por um determinado nível de informação.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-121">The following table shows the data returned by a given information level.</span></span>



| <span data-ttu-id="c5ba1-122">Nível de informações</span><span class="sxs-lookup"><span data-stu-id="c5ba1-122">Information level</span></span>                 | <span data-ttu-id="c5ba1-123">Dados retornados</span><span class="sxs-lookup"><span data-stu-id="c5ba1-123">Data returned</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ba1-124">**BatteryDeviceName**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-124">**BatteryDeviceName**</span></span>             | <span data-ttu-id="c5ba1-125">Cadeia de caracteres Unicode terminada em **nulo** que especifica o nome da bateria.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-125">**Null**-terminated Unicode string that specifies the battery's name.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c5ba1-126">**BatteryEstimatedTime**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-126">**BatteryEstimatedTime**</span></span>          | <span data-ttu-id="c5ba1-127">Um **ULONG** que especifica o tempo de execução de bateria estimado, em segundos.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-127">A **ULONG** that specifies estimated battery run time, in seconds.</span></span> <span data-ttu-id="c5ba1-128">Se a taxa de dreno fornecida no membro **AtRate** da estrutura de [**\_ \_ informações de consulta da bateria**](battery-query-information-str.md) for zero, esse cálculo será baseado na taxa atual de drenagem.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-128">If the rate of drain provided in the **AtRate** member of the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure is zero, this calculation is based on the present rate of drain.</span></span> <span data-ttu-id="c5ba1-129">Se **AtRate** for diferente de zero, o tempo retornado será o tempo de execução esperado para a taxa determinada.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-129">If **AtRate** is nonzero, the time returned is the expected run time for the given rate.</span></span> <span data-ttu-id="c5ba1-130">Se o tempo estimado for desconhecido (por exemplo, a bateria não está sendo descarregada e **AtRate** for zero), o **\_ \_ tempo de bateria desconhecido** será retornado.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-130">If the estimated time is unknown (for example, the battery is not discharging and **AtRate** is zero), **BATTERY\_UNKNOWN\_TIME** is returned.</span></span> <span data-ttu-id="c5ba1-131">Observe que esse valor não é muito preciso em alguns sistemas de bateria.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-131">Note that this value is not very accurate on some battery systems.</span></span> <span data-ttu-id="c5ba1-132">O valor pode variar muito, dependendo do consumo de energia presente, que pode ser afetado pela atividade de disco e por outros fatores.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-132">The value may vary widely depending on present power usage, which could be affected by disk activity and other factors.</span></span> <span data-ttu-id="c5ba1-133">Não há nenhum mecanismo de notificação para alterações nesse valor.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-133">There is no notification mechanism for changes in this value.</span></span> |
| <span data-ttu-id="c5ba1-134">**BatteryGranularityInformation**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-134">**BatteryGranularityInformation**</span></span> | <span data-ttu-id="c5ba1-135">Uma matriz de comprimento variável de estruturas de [**\_ \_ escala de relatório de bateria**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) que contém a granularidade do relatório para a capacidade da bateria retornada do [**\_ \_ \_ status da consulta da bateria do IOCTL**](ioctl-battery-query-status.md).</span><span class="sxs-lookup"><span data-stu-id="c5ba1-135">A variable-length array of [**BATTERY\_REPORTING\_SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) structures that contains the reporting granularity for the battery capacity that is returned from [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md).</span></span> <span data-ttu-id="c5ba1-136">Várias entradas são retornadas quando a granularidade depende da capacidade presente da bateria.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-136">Multiple entries are returned when the granularity depends on the present capacity of the battery.</span></span> <span data-ttu-id="c5ba1-137">Consulte **\_ \_ escala de relatório de bateria** para a interpretação da matriz de entradas.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-137">See **BATTERY\_REPORTING\_SCALE** for the interpretation of the array of entries.</span></span> <span data-ttu-id="c5ba1-138">O número de entradas é indicado pelo tamanho do buffer retornado e pode ser calculado como (*lpBytesReturned* /sizeof (**escala de relatório de \_ bateria \_**)).</span><span class="sxs-lookup"><span data-stu-id="c5ba1-138">The number of entries is indicated by the size of the buffer returned, and can be calculated as (*lpBytesReturned* / sizeof (**BATTERY\_REPORTING\_SCALE**)).</span></span> <span data-ttu-id="c5ba1-139">O número máximo de entradas que serão retornadas é quatro.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-139">The maximum number of entries that will be returned is four.</span></span>                                                                                                |
| <span data-ttu-id="c5ba1-140">**BatteryInformation**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-140">**BatteryInformation**</span></span>            | <span data-ttu-id="c5ba1-141">Uma estrutura de [**\_ informações da bateria**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ba1-141">A [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c5ba1-142">**BatteryManufactureDate**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-142">**BatteryManufactureDate**</span></span>        | <span data-ttu-id="c5ba1-143">Uma estrutura de [**\_ \_ data de fabricação de bateria**](battery-manufacture-date-str.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ba1-143">A [**BATTERY\_MANUFACTURE\_DATE**](battery-manufacture-date-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c5ba1-144">**BatteryManufactureName**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-144">**BatteryManufactureName**</span></span>        | <span data-ttu-id="c5ba1-145">Cadeia de caracteres Unicode terminada em **nulo** que contém o nome do fabricante da bateria.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-145">**Null**-terminated Unicode string that contains the name of the manufacturer of the battery.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c5ba1-146">**BatterySerialNumber**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-146">**BatterySerialNumber**</span></span>           | <span data-ttu-id="c5ba1-147">Cadeia de caracteres Unicode terminada em **nulo** que contém o número de série da bateria.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-147">**Null**-terminated Unicode string that contains the battery's serial number.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c5ba1-148">**BatteryTemperature**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-148">**BatteryTemperature**</span></span>            | <span data-ttu-id="c5ba1-149">Um **ULONG** que contém a temperatura atual da bateria, em 10 ° de um grau Kelvin.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-149">A **ULONG** that contains the battery's current temperature, in 10ths of a degree Kelvin.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c5ba1-150">**BatteryUniqueID**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-150">**BatteryUniqueID**</span></span>               | <span data-ttu-id="c5ba1-151">Cadeia de caracteres Unicode terminada em **nulo** que identifica exclusivamente a bateria.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-151">**Null**-terminated Unicode string that uniquely identifies the battery.</span></span> <span data-ttu-id="c5ba1-152">Esse valor pode ser usado para rastrear uma bateria específica.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-152">This value can be used to track a specific battery.</span></span> <span data-ttu-id="c5ba1-153">No caso de baterias inteligentes, essa ID será a concatenação do nome do fabricante, do nome do dispositivo, da data de fabricação e de uma representação imprimível do número de série.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-153">In the case of smart batteries, this ID will be the concatenation of the manufacturer's name, device name, date of manufacture, and a printable representation of the serial number.</span></span> <span data-ttu-id="c5ba1-154">Esse valor não deve ser exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-154">This value is not intended to be displayed to the user.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="c5ba1-155">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="c5ba1-155">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba1-156">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-156">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="c5ba1-157">Dependendo do nível de informação dos dados solicitados, esse pode ser um buffer de tamanho de variavelmente.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-157">Depending on the information level of data requested, this may be a variably sized buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba1-158">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="c5ba1-158">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba1-159">Um ponteiro para uma variável que recebe o tamanho dos dados retornados no buffer *lpOutBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-159">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="c5ba1-160">Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro **\_ \_ buffer insuficiente** e o número de bytes retornados será zero.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-160">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="c5ba1-161">Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-161">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="c5ba1-162">Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-162">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="c5ba1-163">Se essa for uma operação sobreposta, você poderá recuperar o número de bytes retornados chamando a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="c5ba1-163">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="c5ba1-164">Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá obter o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="c5ba1-164">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba1-165">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="c5ba1-165">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba1-166">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="c5ba1-166">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="c5ba1-167">Se *hDevice* tiver sido aberto com o sinalizador **\_ \_ sobreposto de sinalizador de arquivo** , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-167">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="c5ba1-168">Nesse caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) é executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="c5ba1-168">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="c5ba1-169">Se o dispositivo tiver sido aberto com o sinalizador **\_ \_ sobreposto de sinalizador de arquivo** e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-169">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="c5ba1-170">Se *hDevice* tiver sido aberto sem especificar o sinalizador **\_ \_ sobreposto do sinalizador de arquivo** , *lpOverlapped* será ignorado e a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-170">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ba1-171">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5ba1-171">Return value</span></span>

<span data-ttu-id="c5ba1-172">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-172">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="c5ba1-173">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-173">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="c5ba1-174">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c5ba1-174">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="c5ba1-175">Algumas informações sobre baterias são opcionais ou podem não fazer sentido para algumas baterias.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-175">Some information about batteries is optional or may be meaningless for some batteries.</span></span> <span data-ttu-id="c5ba1-176">Se o tipo específico de dados solicitado não estiver disponível para a bateria atual, a **\_ \_ função erro inválido** será retornada.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-176">If the particular type of data requested is not available for the current battery, then **ERROR\_INVALID\_FUNCTION** is returned.</span></span>

<span data-ttu-id="c5ba1-177">Todas as solicitações de informações da bateria serão concluídas com o status do **arquivo de erro \_ \_ não \_ encontrado** sempre que o elemento **BatteryTag** da solicitação não corresponder ao da marca da bateria atual.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-177">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="c5ba1-178">Isso garante que as informações de bateria retornadas correspondam àquela da bateria solicitada.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-178">This ensures that the returned battery information matches that of the requested battery.</span></span> <span data-ttu-id="c5ba1-179">(Consulte [marcas de bateria](battery-information.md) para obter mais informações.)</span><span class="sxs-lookup"><span data-stu-id="c5ba1-179">(See [Battery Tags](battery-information.md) for more information.)</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ba1-180">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5ba1-180">Remarks</span></span>

<span data-ttu-id="c5ba1-181">Essa bateria IOCTL recupera uma variedade de informações para a bateria.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-181">This battery IOCTL retrieves a variety of information for the battery.</span></span> <span data-ttu-id="c5ba1-182">A estrutura do parâmetro de entrada, [**\_ \_ as informações de consulta da bateria**](battery-query-information-str.md), indicam o tipo de informações a serem retornadas e quando as informações da bateria devem ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-182">The input parameter structure, [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md), indicates the type of information to be returned and when the battery information should be returned.</span></span> <span data-ttu-id="c5ba1-183">O tipo de dados e o conteúdo do buffer de saída variam com base nos dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="c5ba1-183">The data type and contents of the output buffer vary based on the data requested.</span></span>

<span data-ttu-id="c5ba1-184">Para as implicações da e/s sobreposta nessa operação, consulte a seção comentários do tópico [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="c5ba1-184">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="c5ba1-185">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c5ba1-185">Examples</span></span>

<span data-ttu-id="c5ba1-186">Para obter um exemplo, consulte [enumerando dispositivos de bateria](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="c5ba1-186">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ba1-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5ba1-187">Requirements</span></span>



| <span data-ttu-id="c5ba1-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ba1-188">Requirement</span></span> | <span data-ttu-id="c5ba1-189">Valor</span><span class="sxs-lookup"><span data-stu-id="c5ba1-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ba1-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5ba1-190">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ba1-191">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c5ba1-191">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="c5ba1-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5ba1-192">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ba1-193">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c5ba1-193">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="c5ba1-194">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5ba1-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ba1-195"><dt>Poclass. h; </dt> <dt>BatClass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="c5ba1-195"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ba1-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5ba1-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ba1-197">Informações da bateria</span><span class="sxs-lookup"><span data-stu-id="c5ba1-197">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="c5ba1-198">Códigos de controle de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="c5ba1-198">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="c5ba1-199">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-199">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="c5ba1-200">**\_informações de consulta de bateria \_**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-200">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="c5ba1-201">**\_escala de relatório de bateria \_**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-201">**BATTERY\_REPORTING\_SCALE**</span></span>](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[<span data-ttu-id="c5ba1-202">**\_status de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-202">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="c5ba1-203">**\_marca de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-203">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="c5ba1-204">**\_informações do \_ conjunto de baterias do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="c5ba1-204">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

