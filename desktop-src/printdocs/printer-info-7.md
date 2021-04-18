---
description: A \_ estrutura informações da impressora \_ 7 especifica informações sobre a impressora dos serviços de diretório.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: Estrutura de PRINTER_INFO_7 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793661"
---
# <a name="printer_info_7-structure"></a><span data-ttu-id="e9ebd-103">Estrutura de informações da impressora \_ \_ 7</span><span class="sxs-lookup"><span data-stu-id="e9ebd-103">PRINTER\_INFO\_7 structure</span></span>

<span data-ttu-id="e9ebd-104">A **estrutura \_ informações \_ da impressora 7** especifica informações sobre a impressora dos serviços de diretório.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-104">The **PRINTER\_INFO\_7** structure specifies directory services printer information.</span></span> <span data-ttu-id="e9ebd-105">Use essa estrutura com a função [**Setprintr**](setprinter.md) para publicar os dados de uma impressora no serviço de diretório (DS) ou para atualizar ou remover os dados publicados de uma impressora do DS.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-105">Use this structure with the [**SetPrinter**](setprinter.md) function to publish a printer's data in the directory service (DS), or to update or remove a printer's published data from the DS.</span></span> <span data-ttu-id="e9ebd-106">Use essa estrutura com a função [**Getprinter**](getprinter.md) para determinar se uma impressora é publicada no DS.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-106">Use this structure with the [**GetPrinter**](getprinter.md) function to determine whether a printer is published in the DS.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ebd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9ebd-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a><span data-ttu-id="e9ebd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e9ebd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9ebd-109">**pszObjectGUID**</span><span class="sxs-lookup"><span data-stu-id="e9ebd-109">**pszObjectGUID**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebd-110">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o GUID do objeto de fila de impressão do serviço de diretório associado a uma impressora publicada.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-110">A pointer to a null-terminated string containing the GUID of the directory service print queue object associated with a published printer.</span></span> <span data-ttu-id="e9ebd-111">Use a função [**Getprintr**](getprinter.md) para recuperar esse GUID.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-111">Use the [**GetPrinter**](getprinter.md) function to retrieve this GUID.</span></span>

<span data-ttu-id="e9ebd-112">Antes de chamar [**Setprinter**](setprinter.md), defina **pszObjectGUID** como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-112">Before calling [**SetPrinter**](setprinter.md), set **pszObjectGUID** to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e9ebd-113">**dwAction**</span><span class="sxs-lookup"><span data-stu-id="e9ebd-113">**dwAction**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebd-114">Indica a ação da função [**Setprinter**](setprinter.md) a ser executada.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-114">Indicates the action for the [**SetPrinter**](setprinter.md) function to perform.</span></span> <span data-ttu-id="e9ebd-115">Para a função [**Getprinter**](getprinter.md) , esse membro indica se a impressora especificada foi publicada.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-115">For the [**GetPrinter**](getprinter.md) function, this member indicates whether the specified printer is published.</span></span> <span data-ttu-id="e9ebd-116">Esse membro pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-116">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="e9ebd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e9ebd-117">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="e9ebd-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e9ebd-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <span data-ttu-id="e9ebd-119"><dt>**DSPRINT \_**</dt> <dt>0x80000000</dt> pendente</span><span class="sxs-lookup"><span data-stu-id="e9ebd-119"><dt>**DSPRINT\_PENDING**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="e9ebd-120">[**Getprinter**](getprinter.md): indica que o sistema está tentando concluir uma operação de publicação ou cancelamento de publicação iniciada por uma chamada [**setprinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="e9ebd-120">[**GetPrinter**](getprinter.md): Indicates that the system is attempting to complete a publish or unpublish operation started by a [**SetPrinter**](setprinter.md) call.</span></span><br/> <span data-ttu-id="e9ebd-121">[**Setprinter**](setprinter.md): esse valor não é válido.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-121">[**SetPrinter**](setprinter.md): This value is not valid.</span></span> <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <span data-ttu-id="e9ebd-122"><dt>**DSPRINT \_ PUBLICAR**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e9ebd-122"><dt>**DSPRINT\_PUBLISH**</dt> <dt>0x00000001</dt></span></span> </dl>       | <span data-ttu-id="e9ebd-123">[**Setprinter**](setprinter.md): publica os dados da impressora no DS.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-123">[**SetPrinter**](setprinter.md): Publishes the printer's data in the DS.</span></span><br/> <span data-ttu-id="e9ebd-124">[**Getprinter**](getprinter.md): indica que a impressora foi publicada.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-124">[**GetPrinter**](getprinter.md): Indicates the printer is published.</span></span> <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <span data-ttu-id="e9ebd-125"><dt>**DSPRINT \_ Republicar**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="e9ebd-125"><dt>**DSPRINT\_REPUBLISH**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="e9ebd-126">[**Setprinter**](setprinter.md): os dados DS da impressora não são publicados e, em seguida, publicados novamente, atualizando todas as propriedades na impressora publicada.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-126">[**SetPrinter**](setprinter.md): The DS data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="e9ebd-127">A nova publicação também altera o GUID da impressora publicada.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-127">Re-publishing also changes the GUID of the published printer.</span></span><br/> <span data-ttu-id="e9ebd-128">[**Getprinter**](getprinter.md): nunca retorna esse valor.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-128">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <span data-ttu-id="e9ebd-129"><dt>**DSPRINT \_ Cancelar publicação**</dt> de <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="e9ebd-129"><dt>**DSPRINT\_UNPUBLISH**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="e9ebd-130">[**Setprinter**](setprinter.md): remove os dados publicados da impressora do DS.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-130">[**SetPrinter**](setprinter.md): Removes the printer's published data from the DS.</span></span><br/> <span data-ttu-id="e9ebd-131">[**Getprinter**](getprinter.md): indica que a impressora não está publicada.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-131">[**GetPrinter**](getprinter.md): Indicates the printer is not published.</span></span> <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <span data-ttu-id="e9ebd-132"><dt>**DSPRINT \_ ATUALIZAÇÃO**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e9ebd-132"><dt>**DSPRINT\_UPDATE**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="e9ebd-133">[**Setprinter**](setprinter.md): atualiza os dados publicados da impressora no DS.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-133">[**SetPrinter**](setprinter.md): Updates the printer's published data in the DS.</span></span><br/> <span data-ttu-id="e9ebd-134">[**Getprinter**](getprinter.md): nunca retorna esse valor.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-134">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9ebd-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9ebd-135">Remarks</span></span>

<span data-ttu-id="e9ebd-136">A estrutura de **informações da impressora \_ \_ 7** é usada em uma chamada de [**reimpressões**](setprinter.md) para publicar informações da impressora no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-136">The **PRINTER\_INFO\_7** structure is used in a [**SetPrinter**](setprinter.md) call to publish printer information to the directory service.</span></span> <span data-ttu-id="e9ebd-137">Os dados publicados incluem todos os valores e dados da impressora especificada encontrados na chave do \_ spooler SPLDS \_ , chave de \_ Driver SPLDS \_ ou chaves de \_ chave de usuário SPLDS \_ criadas [**por SetPrinterDataEx**](setprinterdataex.md).</span><span class="sxs-lookup"><span data-stu-id="e9ebd-137">The published data includes all values and data for the specified printer found under the SPLDS\_SPOOLER\_KEY, SPLDS\_DRIVER\_KEY, or SPLDS\_USER\_KEY keys created by [**SetPrinterDataEx**](setprinterdataex.md).</span></span>

<span data-ttu-id="e9ebd-138">Para [**Setprinter**](setprinter.md), *pszObjectGUID* deve ser definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-138">For [**SetPrinter**](setprinter.md), *pszObjectGUID* should be set to **NULL**.</span></span> <span data-ttu-id="e9ebd-139">Para [**Getprinter**](getprinter.md), *PSZOBJECTGUID* retorna o GUID do objeto de fila de impressão dos serviços de diretório associado a uma impressora publicada.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-139">For [**GetPrinter**](getprinter.md), *pszObjectGUID* returns the GUID of the directory services print queue object associated with a published printer.</span></span> <span data-ttu-id="e9ebd-140">Você pode usar esse GUID com métodos de interface de serviços de Active Directory (ADSI) para recuperar dados publicados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="e9ebd-140">You can use this GUID with Active Directory Services Interface (ADSI) methods to retrieve published data for the printer.</span></span> <span data-ttu-id="e9ebd-141">No entanto, o método recomendado para recuperar dados publicados é chamar a função [**GetPrinterDataEx**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="e9ebd-141">However, the recommended method for retrieving published data is to call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ebd-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9ebd-142">Requirements</span></span>



| <span data-ttu-id="e9ebd-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ebd-143">Requirement</span></span> | <span data-ttu-id="e9ebd-144">Valor</span><span class="sxs-lookup"><span data-stu-id="e9ebd-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ebd-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ebd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ebd-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9ebd-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e9ebd-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ebd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ebd-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9ebd-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e9ebd-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e9ebd-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ebd-150"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9ebd-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e9ebd-151">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e9ebd-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e9ebd-152">**\_ Informações de impressora \_ \_ 7W** (Unicode) e **\_ informações de impressora \_ \_ 7a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e9ebd-152">**\_PRINTER\_INFO\_7W** (Unicode) and **\_PRINTER\_INFO\_7A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="e9ebd-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9ebd-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ebd-154">Impressão</span><span class="sxs-lookup"><span data-stu-id="e9ebd-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e9ebd-155">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e9ebd-155">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




