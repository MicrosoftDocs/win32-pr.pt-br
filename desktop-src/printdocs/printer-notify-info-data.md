---
description: A \_ estrutura de dados informações de notificação de impressora \_ \_ identifica um campo de informações de trabalho ou impressora e fornece os dados atuais para esse campo.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: Estrutura de PRINTER_NOTIFY_INFO_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169932"
---
# <a name="printer_notify_info_data-structure"></a><span data-ttu-id="7d6f5-103">\_Estrutura de \_ dados de informações de notificação de impressora \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-103">PRINTER\_NOTIFY\_INFO\_DATA structure</span></span>

<span data-ttu-id="7d6f5-104">A estrutura de **\_ \_ \_ dados informações de notificação de impressora** identifica um campo de informações de trabalho ou impressora e fornece os dados atuais para esse campo.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-104">The **PRINTER\_NOTIFY\_INFO\_DATA** structure identifies a job or printer information field and provides the current data for that field.</span></span>

<span data-ttu-id="7d6f5-105">A função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) retorna uma estrutura de [**\_ \_ informações de notificação de impressora**](printer-notify-info.md) , que contém uma matriz de estruturas de **\_ \_ \_ dados de informações de notificação de impressora** .</span><span class="sxs-lookup"><span data-stu-id="7d6f5-105">The [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function returns a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of **PRINTER\_NOTIFY\_INFO\_DATA** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6f5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d6f5-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a><span data-ttu-id="7d6f5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7d6f5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d6f5-108">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="7d6f5-109">Indica o tipo de informação fornecido.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-109">Indicates the type of information provided.</span></span> <span data-ttu-id="7d6f5-110">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="7d6f5-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7d6f5-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="7d6f5-112">Significado</span><span class="sxs-lookup"><span data-stu-id="7d6f5-112">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="7d6f5-113"><dt>**Trabalho \_ do NOTIFICAr \_ tipo**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="7d6f5-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="7d6f5-114">Indica que o membro de **campo** especifica uma \_ constante de campo de notificação de trabalho \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="7d6f5-114">Indicates that the **Field** member specifies a JOB\_NOTIFY\_FIELD\_\* constant.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="7d6f5-115"><dt>**Impressora \_ NOTIFICAr \_ tipo**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="7d6f5-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="7d6f5-116">Indica que o membro de **campo** especifica uma \_ constante de campo de notificação de impressora \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="7d6f5-116">Indicates that the **Field** member specifies a PRINTER\_NOTIFY\_FIELD\_\* constant.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d6f5-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-117">**Field**</span></span>
</dt> <dd>

<span data-ttu-id="7d6f5-118">Indica o campo que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-118">Indicates the field that changed.</span></span> <span data-ttu-id="7d6f5-119">Para obter uma lista de valores possíveis, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-119">For a list of possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="7d6f5-120">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-120">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="7d6f5-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7d6f5-122">**Id**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-122">**Id**</span></span>
</dt> <dd>

<span data-ttu-id="7d6f5-123">Indica o identificador de trabalho se o membro de **tipo** especificar o tipo de notificação de trabalho \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7d6f5-123">Indicates the job identifier if the **Type** member specifies JOB\_NOTIFY\_TYPE.</span></span> <span data-ttu-id="7d6f5-124">Se o **tipo** membro especificar \_ \_ tipo de notificação de impressora, esse membro será indefinido.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-124">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="7d6f5-125">**NotifyData**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-125">**NotifyData**</span></span>
</dt> <dd>

<span data-ttu-id="7d6f5-126">Uma União de informações de dados com base nos membros de **tipo** e **campo** .</span><span class="sxs-lookup"><span data-stu-id="7d6f5-126">A union of data information based on the **Type** and **Field** members.</span></span> <span data-ttu-id="7d6f5-127">Para obter uma descrição do tipo de dados associado a cada campo, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-127">For a description of the type of data associated with each field, see the Remarks section.</span></span>

<dl> <dt>

<span data-ttu-id="7d6f5-128">**adwData \[ 2\]**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-128">**adwData\[2\]**</span></span>
</dt> <dd>

<span data-ttu-id="7d6f5-129">Uma matriz de dois valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7d6f5-129">An array of two **DWORD** values.</span></span> <span data-ttu-id="7d6f5-130">Para campos de informações que usam apenas uma única **DWORD**, os dados estão em **adwData** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="7d6f5-130">For information fields that use only a single **DWORD**, the data is in **adwData** \[0\].</span></span>

</dd> <dt>

<span data-ttu-id="7d6f5-131">**Dados**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-131">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d6f5-132">**cbBuf**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-132">**cbBuf**</span></span>
</dt> <dd>

<span data-ttu-id="7d6f5-133">Indica o tamanho, em bytes, do buffer apontado por **pBuf**.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-133">Indicates the size, in bytes, of the buffer pointed to by **pBuf**.</span></span>

</dd> <dt>

<span data-ttu-id="7d6f5-134">**pBuf**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-134">**pBuf**</span></span>
</dt> <dd>

<span data-ttu-id="7d6f5-135">Ponteiro para um buffer que contém os dados atuais do campo.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-135">Pointer to a buffer that contains the field's current data.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d6f5-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d6f5-136">Remarks</span></span>

<span data-ttu-id="7d6f5-137">Se o **tipo** membro especificar \_ tipo de notificação de impressora \_ , o membro de **campo** poderá ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-137">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7d6f5-138">Campo</span><span class="sxs-lookup"><span data-stu-id="7d6f5-138">Field</span></span></th>
<th><span data-ttu-id="7d6f5-139">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7d6f5-139">Type of data</span></span></th>
<th><span data-ttu-id="7d6f5-140">Valor</span><span class="sxs-lookup"><span data-stu-id="7d6f5-140">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d6f5-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7d6f5-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span></span></td>
<td><span data-ttu-id="7d6f5-142">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-142">Not supported.</span></span></td>
<td><span data-ttu-id="7d6f5-143">0x00</span><span class="sxs-lookup"><span data-stu-id="7d6f5-143">0x00</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span><span class="sxs-lookup"><span data-stu-id="7d6f5-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span></span></td>
<td><span data-ttu-id="7d6f5-145"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-145"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer.</span></span></td>
<td><span data-ttu-id="7d6f5-146">0x01</span><span class="sxs-lookup"><span data-stu-id="7d6f5-146">0x01</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span><span class="sxs-lookup"><span data-stu-id="7d6f5-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span></span></td>
<td><span data-ttu-id="7d6f5-148"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que identifica o ponto de compartilhamento da impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-148"><strong>pBuf</strong> is a pointer to a null-terminated string that identifies the share point for the printer.</span></span></td>
<td><span data-ttu-id="7d6f5-149">0x02</span><span class="sxs-lookup"><span data-stu-id="7d6f5-149">0x02</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span><span class="sxs-lookup"><span data-stu-id="7d6f5-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span></span></td>
<td><span data-ttu-id="7d6f5-151"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da porta na qual os trabalhos de impressão serão impressos.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-151"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the port that the print jobs will be printed to.</span></span> <span data-ttu-id="7d6f5-152">Se &quot; &quot; o pool de impressoras estiver selecionado, essa será uma lista de portas separadas por vírgula.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-152">If &quot;Printer Pooling&quot; is selected, this is a comma separated list of ports.</span></span></td>
<td><span data-ttu-id="7d6f5-153">0x03</span><span class="sxs-lookup"><span data-stu-id="7d6f5-153">0x03</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7d6f5-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span></span></td>
<td><span data-ttu-id="7d6f5-155"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do driver da impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-155"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer's driver.</span></span></td>
<td><span data-ttu-id="7d6f5-156">0x04</span><span class="sxs-lookup"><span data-stu-id="7d6f5-156">0x04</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-157">PRINTER_NOTIFY_FIELD_COMMENT</span><span class="sxs-lookup"><span data-stu-id="7d6f5-157">PRINTER_NOTIFY_FIELD_COMMENT</span></span></td>
<td><span data-ttu-id="7d6f5-158"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém a nova cadeia de caracteres de comentário, que normalmente é uma breve descrição da impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-158"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new comment string, which is typically a brief description of the printer.</span></span></td>
<td><span data-ttu-id="7d6f5-159">0x05</span><span class="sxs-lookup"><span data-stu-id="7d6f5-159">0x05</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-160">PRINTER_NOTIFY_FIELD_LOCATION</span><span class="sxs-lookup"><span data-stu-id="7d6f5-160">PRINTER_NOTIFY_FIELD_LOCATION</span></span></td>
<td><span data-ttu-id="7d6f5-161"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o novo local físico da impressora (por exemplo, &quot; Bldg.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-161"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new physical location of the printer (for example, &quot;Bldg.</span></span> <span data-ttu-id="7d6f5-162">38, sala 1164 &quot; ).</span><span class="sxs-lookup"><span data-stu-id="7d6f5-162">38, Room 1164&quot;).</span></span></td>
<td><span data-ttu-id="7d6f5-163">0x06</span><span class="sxs-lookup"><span data-stu-id="7d6f5-163">0x06</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-164">PRINTER_NOTIFY_FIELD_DEVMODE</span><span class="sxs-lookup"><span data-stu-id="7d6f5-164">PRINTER_NOTIFY_FIELD_DEVMODE</span></span></td>
<td><span data-ttu-id="7d6f5-165"><strong>pBuf</strong> é um ponteiro para uma estrutura <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> que define dados de impressora padrão, como a orientação do papel e a resolução.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-165"><strong>pBuf</strong> is a pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> structure that defines default printer data such as the paper orientation and the resolution.</span></span></td>
<td><span data-ttu-id="7d6f5-166">0x07</span><span class="sxs-lookup"><span data-stu-id="7d6f5-166">0x07</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-167">PRINTER_NOTIFY_FIELD_SEPFILE</span><span class="sxs-lookup"><span data-stu-id="7d6f5-167">PRINTER_NOTIFY_FIELD_SEPFILE</span></span></td>
<td><span data-ttu-id="7d6f5-168"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do arquivo usado para criar a página separadora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-168"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="7d6f5-169">Esta página é usada para separar trabalhos de impressão enviados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-169">This page is used to separate print jobs sent to the printer.</span></span></td>
<td><span data-ttu-id="7d6f5-170">0x08</span><span class="sxs-lookup"><span data-stu-id="7d6f5-170">0x08</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="7d6f5-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span></span></td>
<td><span data-ttu-id="7d6f5-172"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão usado pela impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-172"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span></td>
<td><span data-ttu-id="7d6f5-173">0x09</span><span class="sxs-lookup"><span data-stu-id="7d6f5-173">0x09</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d6f5-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span></span></td>
<td><span data-ttu-id="7d6f5-175"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os parâmetros de processador de impressão padrão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-175"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the default print-processor parameters.</span></span></td>
<td><span data-ttu-id="7d6f5-176">0x0A</span><span class="sxs-lookup"><span data-stu-id="7d6f5-176">0x0A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-177">PRINTER_NOTIFY_FIELD_DATATYPE</span><span class="sxs-lookup"><span data-stu-id="7d6f5-177">PRINTER_NOTIFY_FIELD_DATATYPE</span></span></td>
<td><span data-ttu-id="7d6f5-178"><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-178"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the data type used to record the print job.</span></span></td>
<td><span data-ttu-id="7d6f5-179">0x0B</span><span class="sxs-lookup"><span data-stu-id="7d6f5-179">0x0B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="7d6f5-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span></span></td>
<td><span data-ttu-id="7d6f5-181"><strong>pBuf</strong> é um ponteiro para uma estrutura de <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> para a impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-181"><strong>pBuf</strong> is a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> structure for the printer.</span></span> <span data-ttu-id="7d6f5-182">O ponteiro pode ser <strong>nulo</strong> se não houver nenhum descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-182">The pointer may be <strong>NULL</strong> if there is no security descriptor.</span></span></td>
<td><span data-ttu-id="7d6f5-183">0x0C</span><span class="sxs-lookup"><span data-stu-id="7d6f5-183">0x0C</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="7d6f5-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span></span></td>
<td><span data-ttu-id="7d6f5-185"><strong>adwData</strong> [0] Especifica os atributos da impressora, que podem ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7d6f5-185"><strong>adwData</strong> [0] specifies the printer attributes, which can be one of the following values:</span></span><dl> <span data-ttu-id="7d6f5-186">PRINTER_ATTRIBUTE_QUEUED</span><span class="sxs-lookup"><span data-stu-id="7d6f5-186">PRINTER_ATTRIBUTE_QUEUED</span></span><br />
<span data-ttu-id="7d6f5-187">PRINTER_ATTRIBUTE_DIRECT</span><span class="sxs-lookup"><span data-stu-id="7d6f5-187">PRINTER_ATTRIBUTE_DIRECT</span></span><br />
<span data-ttu-id="7d6f5-188">PRINTER_ATTRIBUTE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7d6f5-188">PRINTER_ATTRIBUTE_DEFAULT</span></span><br />
<span data-ttu-id="7d6f5-189">PRINTER_ATTRIBUTE_SHARED</span><span class="sxs-lookup"><span data-stu-id="7d6f5-189">PRINTER_ATTRIBUTE_SHARED</span></span><br />
</dl></td>
<td><span data-ttu-id="7d6f5-190">0x0D</span><span class="sxs-lookup"><span data-stu-id="7d6f5-190">0x0D</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-191">PRINTER_NOTIFY_FIELD_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="7d6f5-191">PRINTER_NOTIFY_FIELD_PRIORITY</span></span></td>
<td><span data-ttu-id="7d6f5-192"><strong>adwData</strong> [0] Especifica um valor de prioridade que o spooler usa para rotear trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-192"><strong>adwData</strong> [0] specifies a priority value that the spooler uses to route print jobs.</span></span></td>
<td><span data-ttu-id="7d6f5-193">0x0E</span><span class="sxs-lookup"><span data-stu-id="7d6f5-193">0x0E</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="7d6f5-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span></span></td>
<td><span data-ttu-id="7d6f5-195"><strong>adwData</strong> [0] Especifica o valor de prioridade padrão atribuído a cada trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-195"><strong>adwData</strong> [0] specifies the default priority value assigned to each print job.</span></span></td>
<td><span data-ttu-id="7d6f5-196">0x0F</span><span class="sxs-lookup"><span data-stu-id="7d6f5-196">0x0F</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-197">PRINTER_NOTIFY_FIELD_START_TIME</span><span class="sxs-lookup"><span data-stu-id="7d6f5-197">PRINTER_NOTIFY_FIELD_START_TIME</span></span></td>
<td><span data-ttu-id="7d6f5-198"><strong>adwData</strong> [0] Especifica a hora mais antiga em que a impressora imprimirá um trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-198"><strong>adwData</strong> [0] specifies the earliest time at which the printer will print a job.</span></span> <span data-ttu-id="7d6f5-199">(Esse valor é especificado em minutos decorridos desde 12:00 A.M.)</span><span class="sxs-lookup"><span data-stu-id="7d6f5-199">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="7d6f5-200">0x10</span><span class="sxs-lookup"><span data-stu-id="7d6f5-200">0x10</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span><span class="sxs-lookup"><span data-stu-id="7d6f5-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span></span></td>
<td><span data-ttu-id="7d6f5-202"><strong>adwData</strong> [0] Especifica a hora mais recente em que a impressora imprimirá um trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-202"><strong>adwData</strong> [0] specifies the latest time at which the printer will print a job.</span></span> <span data-ttu-id="7d6f5-203">(Esse valor é especificado em minutos decorridos desde 12:00 A.M.)</span><span class="sxs-lookup"><span data-stu-id="7d6f5-203">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="7d6f5-204">0x11</span><span class="sxs-lookup"><span data-stu-id="7d6f5-204">0x11</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-205">PRINTER_NOTIFY_FIELD_STATUS</span><span class="sxs-lookup"><span data-stu-id="7d6f5-205">PRINTER_NOTIFY_FIELD_STATUS</span></span></td>
<td><span data-ttu-id="7d6f5-206"><strong>adwData</strong> [0] Especifica o status da impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-206"><strong>adwData</strong> [0] specifies the printer status.</span></span> <span data-ttu-id="7d6f5-207">Para obter uma lista de valores possíveis, consulte a estrutura de <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7d6f5-207">For a list of possible values, see the <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> structure.</span></span></td>
<td><span data-ttu-id="7d6f5-208">0x12</span><span class="sxs-lookup"><span data-stu-id="7d6f5-208">0x12</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span><span class="sxs-lookup"><span data-stu-id="7d6f5-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span></span></td>
<td><span data-ttu-id="7d6f5-210">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-210">Not supported.</span></span></td>
<td><span data-ttu-id="7d6f5-211">0x13</span><span class="sxs-lookup"><span data-stu-id="7d6f5-211">0x13</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-212">PRINTER_NOTIFY_FIELD_CJOBS</span><span class="sxs-lookup"><span data-stu-id="7d6f5-212">PRINTER_NOTIFY_FIELD_CJOBS</span></span></td>
<td><span data-ttu-id="7d6f5-213"><strong>adwData</strong> [0] Especifica o número de trabalhos de impressão que foram enfileirados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-213"><strong>adwData</strong> [0] specifies the number of print jobs that have been queued for the printer.</span></span></td>
<td><span data-ttu-id="7d6f5-214">0x14</span><span class="sxs-lookup"><span data-stu-id="7d6f5-214">0x14</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span><span class="sxs-lookup"><span data-stu-id="7d6f5-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span></span></td>
<td><span data-ttu-id="7d6f5-216"><strong>adwData</strong> [0] Especifica o número médio de páginas por minuto que foram impressas na impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-216"><strong>adwData</strong> [0] specifies the average number of pages per minute that have been printed on the printer.</span></span></td>
<td><span data-ttu-id="7d6f5-217">0x15</span><span class="sxs-lookup"><span data-stu-id="7d6f5-217">0x15</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span><span class="sxs-lookup"><span data-stu-id="7d6f5-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span></span></td>
<td><span data-ttu-id="7d6f5-219">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-219">Not supported.</span></span></td>
<td><span data-ttu-id="7d6f5-220">0x16</span><span class="sxs-lookup"><span data-stu-id="7d6f5-220">0x16</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="7d6f5-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span></span></td>
<td><span data-ttu-id="7d6f5-222">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-222">Not supported.</span></span></td>
<td><span data-ttu-id="7d6f5-223">0x17</span><span class="sxs-lookup"><span data-stu-id="7d6f5-223">0x17</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span><span class="sxs-lookup"><span data-stu-id="7d6f5-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span></span></td>
<td><span data-ttu-id="7d6f5-225">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-225">Not supported.</span></span></td>
<td><span data-ttu-id="7d6f5-226">0x18</span><span class="sxs-lookup"><span data-stu-id="7d6f5-226">0x18</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="7d6f5-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span></span></td>
<td><span data-ttu-id="7d6f5-228">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-228">Not supported.</span></span></td>
<td><span data-ttu-id="7d6f5-229">0x19</span><span class="sxs-lookup"><span data-stu-id="7d6f5-229">0x19</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d6f5-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span><span class="sxs-lookup"><span data-stu-id="7d6f5-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span></span></td>
<td><span data-ttu-id="7d6f5-231">Isso será definido se o GUID do objeto for alterado.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-231">This is set if the object GUID changes.</span></span></td>
<td><span data-ttu-id="7d6f5-232">0x1A</span><span class="sxs-lookup"><span data-stu-id="7d6f5-232">0x1A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6f5-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="7d6f5-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span></span></td>
<td><span data-ttu-id="7d6f5-234">Isso será definido se a conexão de impressora for renomeada.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-234">This is set if the printer connection is renamed.</span></span></td>
<td><span data-ttu-id="7d6f5-235">0x1B</span><span class="sxs-lookup"><span data-stu-id="7d6f5-235">0x1B</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7d6f5-236">Se o membro de **tipo** especificar o tipo de notificação de trabalho \_ \_ , o **campo** membro poderá ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-236">If the **Type** member specifies JOB\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



| <span data-ttu-id="7d6f5-237">Campo</span><span class="sxs-lookup"><span data-stu-id="7d6f5-237">Field</span></span>                                    | <span data-ttu-id="7d6f5-238">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7d6f5-238">Type of data</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="7d6f5-239">Valor</span><span class="sxs-lookup"><span data-stu-id="7d6f5-239">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="7d6f5-240">\_nome da \_ impressora do campo NOTIFICAr trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-240">JOB\_NOTIFY\_FIELD\_PRINTER\_NAME</span></span>        | <span data-ttu-id="7d6f5-241">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da impressora para a qual o trabalho está no spool.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-241">**pBuf** is a pointer to a null-terminated string containing the name of the printer for which the job is spooled.</span></span>                                                                                                                                      | <span data-ttu-id="7d6f5-242">0x00</span><span class="sxs-lookup"><span data-stu-id="7d6f5-242">0x00</span></span>  |
| <span data-ttu-id="7d6f5-243">\_nome da \_ máquina do campo de notificação de trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-243">JOB\_NOTIFY\_FIELD\_MACHINE\_NAME</span></span>        | <span data-ttu-id="7d6f5-244">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do computador que criou o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-244">**pBuf** is a pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>                                                                                                                                    | <span data-ttu-id="7d6f5-245">0x01</span><span class="sxs-lookup"><span data-stu-id="7d6f5-245">0x01</span></span>  |
| <span data-ttu-id="7d6f5-246">\_nome da \_ porta do campo NOTIFICAr trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-246">JOB\_NOTIFY\_FIELD\_PORT\_NAME</span></span>           | <span data-ttu-id="7d6f5-247">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que identifica as portas usadas para transmitir dados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-247">**pBuf** is a pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="7d6f5-248">Se uma impressora estiver conectada a mais de uma porta, os nomes das portas serão separados por vírgulas (por exemplo, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="7d6f5-248">If a printer is connected to more than one port, the names of the ports are separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span> | <span data-ttu-id="7d6f5-249">0x02</span><span class="sxs-lookup"><span data-stu-id="7d6f5-249">0x02</span></span>  |
| <span data-ttu-id="7d6f5-250">\_nome de \_ usuário do campo de notificação de trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-250">JOB\_NOTIFY\_FIELD\_USER\_NAME</span></span>           | <span data-ttu-id="7d6f5-251">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que enviou o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-251">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who sent the print job.</span></span>                                                                                                                                           | <span data-ttu-id="7d6f5-252">0x03</span><span class="sxs-lookup"><span data-stu-id="7d6f5-252">0x03</span></span>  |
| <span data-ttu-id="7d6f5-253">\_nome da \_ notificação do campo de notificação de trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-253">JOB\_NOTIFY\_FIELD\_NOTIFY\_NAME</span></span>         | <span data-ttu-id="7d6f5-254">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que deve ser notificado quando o trabalho tiver sido impresso ou quando ocorrer um erro durante a impressão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-254">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>                                                              | <span data-ttu-id="7d6f5-255">0x04</span><span class="sxs-lookup"><span data-stu-id="7d6f5-255">0x04</span></span>  |
| <span data-ttu-id="7d6f5-256">\_tipo de \_ dados do campo de notificação de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-256">JOB\_NOTIFY\_FIELD\_DATATYPE</span></span>             | <span data-ttu-id="7d6f5-257">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-257">**pBuf** is a pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>                                                                                                                                         | <span data-ttu-id="7d6f5-258">0x05</span><span class="sxs-lookup"><span data-stu-id="7d6f5-258">0x05</span></span>  |
| <span data-ttu-id="7d6f5-259">\_processador de \_ impressão de campo de notificação de trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-259">JOB\_NOTIFY\_FIELD\_PRINT\_PROCESSOR</span></span>     | <span data-ttu-id="7d6f5-260">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão a ser usado para imprimir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-260">**pBuf** is a pointer to a null-terminated string that specifies the name of the print processor to be used to print the job.</span></span>                                                                                                                           | <span data-ttu-id="7d6f5-261">0x06</span><span class="sxs-lookup"><span data-stu-id="7d6f5-261">0x06</span></span>  |
| <span data-ttu-id="7d6f5-262">\_parâmetros de \_ campo de notificação de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-262">JOB\_NOTIFY\_FIELD\_PARAMETERS</span></span>           | <span data-ttu-id="7d6f5-263">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os parâmetros do processador de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-263">**pBuf** is a pointer to a null-terminated string that specifies print-processor parameters.</span></span>                                                                                                                                                            | <span data-ttu-id="7d6f5-264">0x07</span><span class="sxs-lookup"><span data-stu-id="7d6f5-264">0x07</span></span>  |
| <span data-ttu-id="7d6f5-265">\_nome do \_ Driver do campo NOTIFICAr trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-265">JOB\_NOTIFY\_FIELD\_DRIVER\_NAME</span></span>         | <span data-ttu-id="7d6f5-266">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver de impressora que deve ser usado para processar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-266">**pBuf** is a pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>                                                                                                           | <span data-ttu-id="7d6f5-267">0x08</span><span class="sxs-lookup"><span data-stu-id="7d6f5-267">0x08</span></span>  |
| <span data-ttu-id="7d6f5-268">\_DEVMODE do \_ campo de notificação de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-268">JOB\_NOTIFY\_FIELD\_DEVMODE</span></span>              | <span data-ttu-id="7d6f5-269">**pBuf** é um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contém dados de inicialização de dispositivo e de ambiente para o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-269">**pBuf** is a pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>                                                                                                        | <span data-ttu-id="7d6f5-270">0x09</span><span class="sxs-lookup"><span data-stu-id="7d6f5-270">0x09</span></span>  |
| <span data-ttu-id="7d6f5-271">\_status do \_ campo de notificação de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-271">JOB\_NOTIFY\_FIELD\_STATUS</span></span>               | <span data-ttu-id="7d6f5-272">**adwData** \[ 0 \] especifica o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-272">**adwData** \[0\] specifies the job status.</span></span> <span data-ttu-id="7d6f5-273">Para obter uma lista de valores possíveis, consulte a estrutura [**informações do trabalho \_ \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="7d6f5-273">For a list of possible values, see the [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>                                                                                                                        | <span data-ttu-id="7d6f5-274">0x0A</span><span class="sxs-lookup"><span data-stu-id="7d6f5-274">0x0A</span></span>  |
| <span data-ttu-id="7d6f5-275">\_cadeia de \_ status do campo NOTIFICAr trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-275">JOB\_NOTIFY\_FIELD\_STATUS\_STRING</span></span>       | <span data-ttu-id="7d6f5-276">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o status do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-276">**pBuf** is a pointer to a null-terminated string that specifies the status of the print job.</span></span>                                                                                                                                                           | <span data-ttu-id="7d6f5-277">0x0B</span><span class="sxs-lookup"><span data-stu-id="7d6f5-277">0x0B</span></span>  |
| <span data-ttu-id="7d6f5-278">\_ \_ \_ descritor de segurança do campo de notificação de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-278">JOB\_NOTIFY\_FIELD\_SECURITY\_DESCRIPTOR</span></span> | <span data-ttu-id="7d6f5-279">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-279">Not supported.</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="7d6f5-280">0x0C</span><span class="sxs-lookup"><span data-stu-id="7d6f5-280">0x0C</span></span>  |
| <span data-ttu-id="7d6f5-281">\_documento de \_ campo de notificação de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-281">JOB\_NOTIFY\_FIELD\_DOCUMENT</span></span>             | <span data-ttu-id="7d6f5-282">**pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do trabalho de impressão (por exemplo, "MS-WORD: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="7d6f5-282">**pBuf** is a pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>                                                                                                                        | <span data-ttu-id="7d6f5-283">0x0D</span><span class="sxs-lookup"><span data-stu-id="7d6f5-283">0x0D</span></span>  |
| <span data-ttu-id="7d6f5-284">\_prioridade do \_ campo de notificação de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-284">JOB\_NOTIFY\_FIELD\_PRIORITY</span></span>             | <span data-ttu-id="7d6f5-285">**adwData** \[ 0 \] especifica a prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-285">**adwData** \[0\] specifies the job priority.</span></span>                                                                                                                                                                                                           | <span data-ttu-id="7d6f5-286">0x0E</span><span class="sxs-lookup"><span data-stu-id="7d6f5-286">0x0E</span></span>  |
| <span data-ttu-id="7d6f5-287">\_posição do \_ campo de notificação de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-287">JOB\_NOTIFY\_FIELD\_POSITION</span></span>             | <span data-ttu-id="7d6f5-288">**adwData** \[ 0 \] especifica a posição do trabalho na fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-288">**adwData** \[0\] specifies the job's position in the print queue.</span></span>                                                                                                                                                                                      | <span data-ttu-id="7d6f5-289">0x0F</span><span class="sxs-lookup"><span data-stu-id="7d6f5-289">0x0F</span></span>  |
| <span data-ttu-id="7d6f5-290">campo de notificação de trabalho \_ \_ \_ enviado</span><span class="sxs-lookup"><span data-stu-id="7d6f5-290">JOB\_NOTIFY\_FIELD\_SUBMITTED</span></span>            | <span data-ttu-id="7d6f5-291">**pBuf** é um ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica a hora em que o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-291">**pBuf** is a pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>                                                                                                                          | <span data-ttu-id="7d6f5-292">0x10</span><span class="sxs-lookup"><span data-stu-id="7d6f5-292">0x10</span></span>  |
| <span data-ttu-id="7d6f5-293">\_hora de \_ início do campo NOTIFICAr trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-293">JOB\_NOTIFY\_FIELD\_START\_TIME</span></span>          | <span data-ttu-id="7d6f5-294">**adwData** \[ 0 \] especifica a hora mais antiga em que o trabalho pode ser impresso.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-294">**adwData** \[0\] specifies the earliest time that the job can be printed.</span></span> <span data-ttu-id="7d6f5-295">(Esse valor é especificado em minutos decorridos desde 12:00 A.M.)</span><span class="sxs-lookup"><span data-stu-id="7d6f5-295">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                | <span data-ttu-id="7d6f5-296">0x11</span><span class="sxs-lookup"><span data-stu-id="7d6f5-296">0x11</span></span>  |
| <span data-ttu-id="7d6f5-297">campo de notificação de trabalho \_ \_ até a \_ \_ hora</span><span class="sxs-lookup"><span data-stu-id="7d6f5-297">JOB\_NOTIFY\_FIELD\_UNTIL\_TIME</span></span>          | <span data-ttu-id="7d6f5-298">**adwData** \[ 0 \] especifica a hora mais recente em que o trabalho pode ser impresso.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-298">**adwData** \[0\] specifies the latest time that the job can be printed.</span></span> <span data-ttu-id="7d6f5-299">(Esse valor é especificado em minutos decorridos desde 12:00 A.M.)</span><span class="sxs-lookup"><span data-stu-id="7d6f5-299">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                  | <span data-ttu-id="7d6f5-300">0x12</span><span class="sxs-lookup"><span data-stu-id="7d6f5-300">0x12</span></span>  |
| <span data-ttu-id="7d6f5-301">\_hora do \_ campo de notificação de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-301">JOB\_NOTIFY\_FIELD\_TIME</span></span>                 | <span data-ttu-id="7d6f5-302">**adwData** \[ 0 \] especifica o tempo total, em segundos, decorrido desde que o trabalho começou a ser impresso.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-302">**adwData** \[0\] specifies the total time, in seconds, that has elapsed since the job began printing.</span></span>                                                                                                                                                  | <span data-ttu-id="7d6f5-303">0x13</span><span class="sxs-lookup"><span data-stu-id="7d6f5-303">0x13</span></span>  |
| <span data-ttu-id="7d6f5-304">TOTAL de páginas de notificação de trabalho do \_ \_ campo \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-304">JOB\_NOTIFY\_FIELD\_TOTAL\_PAGES</span></span>         | <span data-ttu-id="7d6f5-305">**adwData** \[ 0 \] especifica o tamanho, em páginas, do trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-305">**adwData** \[0\] specifies the size, in pages, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="7d6f5-306">0x14</span><span class="sxs-lookup"><span data-stu-id="7d6f5-306">0x14</span></span>  |
| <span data-ttu-id="7d6f5-307">páginas de campo de notificação de trabalho \_ \_ \_ \_ impressas</span><span class="sxs-lookup"><span data-stu-id="7d6f5-307">JOB\_NOTIFY\_FIELD\_PAGES\_PRINTED</span></span>       | <span data-ttu-id="7d6f5-308">**adwData** \[ 0 \] especifica o número de páginas que foram impressas.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-308">**adwData** \[0\] specifies the number of pages that have printed.</span></span>                                                                                                                                                                                      | <span data-ttu-id="7d6f5-309">0x15</span><span class="sxs-lookup"><span data-stu-id="7d6f5-309">0x15</span></span>  |
| <span data-ttu-id="7d6f5-310">\_total de \_ bytes do campo de notificação de trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d6f5-310">JOB\_NOTIFY\_FIELD\_TOTAL\_BYTES</span></span>         | <span data-ttu-id="7d6f5-311">**adwData** \[ 0 \] especifica o tamanho, em bytes, do trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-311">**adwData** \[0\] specifies the size, in bytes, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="7d6f5-312">0x16</span><span class="sxs-lookup"><span data-stu-id="7d6f5-312">0x16</span></span>  |
| <span data-ttu-id="7d6f5-313">BYTES de campo de notificação de trabalho \_ \_ \_ \_ impressos</span><span class="sxs-lookup"><span data-stu-id="7d6f5-313">JOB\_NOTIFY\_FIELD\_BYTES\_PRINTED</span></span>       | <span data-ttu-id="7d6f5-314">**adwData** \[ 0 \] especifica o número de bytes que foram impressos neste trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-314">**adwData** \[0\] specifies the number of bytes that have been printed on this job.</span></span> <span data-ttu-id="7d6f5-315">Para esse campo, o objeto de notificação de alteração é sinalizado quando bytes são enviados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="7d6f5-315">For this field, the change notification object is signaled when bytes are sent to the printer.</span></span>                                                                      | <span data-ttu-id="7d6f5-316">0x17</span><span class="sxs-lookup"><span data-stu-id="7d6f5-316">0x17</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="7d6f5-317">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d6f5-317">Requirements</span></span>



| <span data-ttu-id="7d6f5-318">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d6f5-318">Requirement</span></span> | <span data-ttu-id="7d6f5-319">Valor</span><span class="sxs-lookup"><span data-stu-id="7d6f5-319">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6f5-320">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d6f5-320">Minimum supported client</span></span><br/> | <span data-ttu-id="7d6f5-321">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d6f5-321">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7d6f5-322">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d6f5-322">Minimum supported server</span></span><br/> | <span data-ttu-id="7d6f5-323">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d6f5-323">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7d6f5-324">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7d6f5-324">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d6f5-325"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d6f5-325"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d6f5-326">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d6f5-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d6f5-327">Impressão</span><span class="sxs-lookup"><span data-stu-id="7d6f5-327">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7d6f5-328">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="7d6f5-328">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7d6f5-329">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-329">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="7d6f5-330">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-330">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="7d6f5-331">**Informações do trabalho \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-331">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="7d6f5-332">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-332">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="7d6f5-333">**\_informações de notificação da impressora \_**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-333">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="7d6f5-334">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-334">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="7d6f5-335">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="7d6f5-335">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

