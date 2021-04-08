---
description: A função EnumPrinters enumera impressoras disponíveis, servidores de impressão, domínios ou provedores de impressão.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Função EnumPrinters (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828315"
---
# <a name="enumprinters-function"></a><span data-ttu-id="06a91-103">Função EnumPrinters</span><span class="sxs-lookup"><span data-stu-id="06a91-103">EnumPrinters function</span></span>

<span data-ttu-id="06a91-104">A função **EnumPrinters** enumera impressoras disponíveis, servidores de impressão, domínios ou provedores de impressão.</span><span class="sxs-lookup"><span data-stu-id="06a91-104">The **EnumPrinters** function enumerates available printers, print servers, domains, or print providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a91-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06a91-105">Syntax</span></span>


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="06a91-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06a91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06a91-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="06a91-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a91-108">Os tipos de objetos de impressão que a função deve enumerar.</span><span class="sxs-lookup"><span data-stu-id="06a91-108">The types of print objects that the function should enumerate.</span></span> <span data-ttu-id="06a91-109">Esse valor pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="06a91-109">This value can be one or more of the following values.</span></span>



| <span data-ttu-id="06a91-110">Valor</span><span class="sxs-lookup"><span data-stu-id="06a91-110">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="06a91-111">Significado</span><span class="sxs-lookup"><span data-stu-id="06a91-111">Meaning</span></span>                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <span data-ttu-id="06a91-112"><dt>**\_local de enumeração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-112"><dt>**PRINTER\_ENUM\_LOCAL**</dt></span></span> </dl>                       | <span data-ttu-id="06a91-113">Se o sinalizador de nome de enumeração da impressora \_ \_ também não for passado, a função ignora o parâmetro de *nome* e enumera as impressoras instaladas localmente.</span><span class="sxs-lookup"><span data-stu-id="06a91-113">If the PRINTER\_ENUM\_NAME flag is not also passed, the function ignores the *Name* parameter, and enumerates the locally installed printers.</span></span> <span data-ttu-id="06a91-114">Se \_ \_ o nome de enumeração da impressora também for passado, a função enumerará as impressoras locais no *nome*.</span><span class="sxs-lookup"><span data-stu-id="06a91-114">If PRINTER\_ENUM\_NAME is also passed, the function enumerates the local printers on *Name*.</span></span> <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <span data-ttu-id="06a91-115"><dt>**\_nome da enumeração da impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-115"><dt>**PRINTER\_ENUM\_NAME**</dt></span></span> </dl>                          | <span data-ttu-id="06a91-116">A função enumera a impressora identificada pelo *nome*.</span><span class="sxs-lookup"><span data-stu-id="06a91-116">The function enumerates the printer identified by *Name*.</span></span> <span data-ttu-id="06a91-117">Pode ser um servidor, um domínio ou um provedor de impressão.</span><span class="sxs-lookup"><span data-stu-id="06a91-117">This can be a server, a domain, or a print provider.</span></span> <span data-ttu-id="06a91-118">Se *Name* for **NULL**, a função enumerará os provedores de impressão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="06a91-118">If *Name* is **NULL**, the function enumerates available print providers.</span></span><br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <span data-ttu-id="06a91-119"><dt>**ENUM de impressora \_ \_ compartilhado**</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-119"><dt>**PRINTER\_ENUM\_SHARED**</dt></span></span> </dl>                    | <span data-ttu-id="06a91-120">A função enumera impressoras que têm o atributo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="06a91-120">The function enumerates printers that have the shared attribute.</span></span> <span data-ttu-id="06a91-121">Não pode ser usado isoladamente; Use uma operação ou para combinar com outro tipo de enumeração de impressora \_ .</span><span class="sxs-lookup"><span data-stu-id="06a91-121">Cannot be used in isolation; use an OR operation to combine with another PRINTER\_ENUM type.</span></span><br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <span data-ttu-id="06a91-122"><dt>**\_conexões de enum de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-122"><dt>**PRINTER\_ENUM\_CONNECTIONS**</dt></span></span> </dl>     | <span data-ttu-id="06a91-123">A função enumera a lista de impressoras para as quais o usuário fez conexões anteriores.</span><span class="sxs-lookup"><span data-stu-id="06a91-123">The function enumerates the list of printers to which the user has made previous connections.</span></span><br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <span data-ttu-id="06a91-124"><dt>**\_rede de enumeração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-124"><dt>**PRINTER\_ENUM\_NETWORK**</dt></span></span> </dl>                 | <span data-ttu-id="06a91-125">A função enumera impressoras de rede no domínio do computador.</span><span class="sxs-lookup"><span data-stu-id="06a91-125">The function enumerates network printers in the computer's domain.</span></span> <span data-ttu-id="06a91-126">Esse valor será válido somente se o *nível* for 1.</span><span class="sxs-lookup"><span data-stu-id="06a91-126">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <span data-ttu-id="06a91-127"><dt>**\_remoto de enumeração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-127"><dt>**PRINTER\_ENUM\_REMOTE**</dt></span></span> </dl>                    | <span data-ttu-id="06a91-128">A função enumera impressoras de rede e servidores de impressão no domínio do computador.</span><span class="sxs-lookup"><span data-stu-id="06a91-128">The function enumerates network printers and print servers in the computer's domain.</span></span> <span data-ttu-id="06a91-129">Esse valor será válido somente se o *nível* for 1.</span><span class="sxs-lookup"><span data-stu-id="06a91-129">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <span data-ttu-id="06a91-130"><dt>**Categoria de enumeração de impressora \_ \_ \_ 3D**</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-130"><dt>**PRINTER\_ENUM\_CATEGORY\_3D**</dt></span></span> </dl>    | <span data-ttu-id="06a91-131">A função enumera somente as impressoras 3D.</span><span class="sxs-lookup"><span data-stu-id="06a91-131">The function enumerates only 3D printers.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <span data-ttu-id="06a91-132"><dt>**Categoria de enumeração de impressora \_ \_ \_ todos**</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-132"><dt>**PRINTER\_ENUM\_CATEGORY\_ALL**</dt></span></span> </dl> | <span data-ttu-id="06a91-133">A função enumera todos os dispositivos de impressão, incluindo impressoras 3D.</span><span class="sxs-lookup"><span data-stu-id="06a91-133">The function enumerates all print devices, including 3D printers.</span></span><br/>                                                                                                                                                                           |



 

<span data-ttu-id="06a91-134">Se o *nível* for 4, você só poderá usar as constantes de enum de impressora e de enumeração de impressoras da impressora \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="06a91-134">If *Level* is 4, you can only use the PRINTER\_ENUM\_CONNECTIONS and PRINTER\_ENUM\_LOCAL constants.</span></span>

> [!Note]  
> <span data-ttu-id="06a91-135">os dispositivos de impressão 3D não são enumerados por padrão.</span><span class="sxs-lookup"><span data-stu-id="06a91-135">3D print devices are not enumerated by default.</span></span> <span data-ttu-id="06a91-136">Você deve incluir a **categoria de enumeração de impressora \_ \_ \_ 3D** e a **enumeração de impressora \_ \_ local** para enumerar somente impressoras 3D.</span><span class="sxs-lookup"><span data-stu-id="06a91-136">You must include both **PRINTER\_ENUM\_CATEGORY\_3D** and **PRINTER\_ENUM\_LOCAL** to enumerate only 3D printers.</span></span> <span data-ttu-id="06a91-137">Para incluir impressoras 3D, juntamente com todas as outras impressoras locais, use a **categoria de enumeração de impressora \_ \_ \_ todos** e a **enumeração de impressora \_ \_ local**.</span><span class="sxs-lookup"><span data-stu-id="06a91-137">To include 3D printers, along with all other local printers, use **PRINTER\_ENUM\_CATEGORY\_ALL** and **PRINTER\_ENUM\_LOCAL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="06a91-138">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="06a91-138">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a91-139">Se o *nível* for 1, os *sinalizadores* contiverem o nome de enumeração da impressora \_ e o \_ *nome* não for **nulo**, o *nome* será um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do objeto a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="06a91-139">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is non-**NULL**, then *Name* is a pointer to a null-terminated string that specifies the name of the object to enumerate.</span></span> <span data-ttu-id="06a91-140">Essa cadeia de caracteres pode ser o nome de um servidor, um domínio ou um provedor de impressão.</span><span class="sxs-lookup"><span data-stu-id="06a91-140">This string can be the name of a server, a domain, or a print provider.</span></span>

<span data-ttu-id="06a91-141">Se o *nível* for 1, os *sinalizadores* contiverem \_ \_ o nome de enumeração da impressora e o *nome* for **nulo**, a função enumerará os provedores de impressão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="06a91-141">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is **NULL**, then the function enumerates the available print providers.</span></span>

<span data-ttu-id="06a91-142">Se *Level* for 1, *flags* contém \_ Remote enum de impressora \_ e *Name* é **NULL**, então a função enumera as impressoras no domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="06a91-142">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_REMOTE, and *Name* is **NULL**, then the function enumerates the printers in the user's domain.</span></span>

<span data-ttu-id="06a91-143">Se *Level* for 2 ou 5,*Name* será um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um servidor cujas impressoras devem ser enumeradas.</span><span class="sxs-lookup"><span data-stu-id="06a91-143">If *Level* is 2 or 5,*Name* is a pointer to a null-terminated string that specifies the name of a server whose printers are to be enumerated.</span></span> <span data-ttu-id="06a91-144">Se essa cadeia de caracteres for **nula**, a função enumerará as impressoras instaladas no computador local.</span><span class="sxs-lookup"><span data-stu-id="06a91-144">If this string is **NULL**, then the function enumerates the printers installed on the local computer.</span></span>

<span data-ttu-id="06a91-145">Se o *nível* for 4, o *nome* deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="06a91-145">If *Level* is 4, *Name* should be **NULL**.</span></span> <span data-ttu-id="06a91-146">A função sempre consulta no computador local.</span><span class="sxs-lookup"><span data-stu-id="06a91-146">The function always queries on the local computer.</span></span>

<span data-ttu-id="06a91-147">Quando o *nome* é **nulo**, a definição de *sinalizadores* para impressora \_ enum \_ impressora local enum \| \_ \_ Connections enumera as impressoras instaladas no computador local.</span><span class="sxs-lookup"><span data-stu-id="06a91-147">When *Name* is **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_CONNECTIONS enumerates printers that are installed on the local machine.</span></span> <span data-ttu-id="06a91-148">Essas impressoras incluem aquelas que estão fisicamente anexadas ao computador local, bem como impressoras remotas às quais ele tem uma conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="06a91-148">These printers include those that are physically attached to the local machine as well as remote printers to which it has a network connection.</span></span>

<span data-ttu-id="06a91-149">Quando o *nome* não for **nulo**, definir *sinalizadores* para impressora \_ enum \_ impressora local \| \_ \_ nome de enumeração enumerará as impressoras locais que estão instaladas no *nome* do servidor.</span><span class="sxs-lookup"><span data-stu-id="06a91-149">When *Name* is not **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_NAME enumerates the local printers that are installed on the server *Name*.</span></span>

</dd> <dt>

<span data-ttu-id="06a91-150">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="06a91-150">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a91-151">O tipo de estruturas de dados apontado por *pPrinterEnum*.</span><span class="sxs-lookup"><span data-stu-id="06a91-151">The type of data structures pointed to by *pPrinterEnum*.</span></span> <span data-ttu-id="06a91-152">Os valores válidos são 1, 2, 4 e 5, que correspondem às estruturas de dados informações da impressora [**\_ \_ 1**](printer-info-1.md), [**informações da impressora \_ \_ 2**](printer-info-2.md) , [**\_ informações \_ 4**](printer-info-4.md)da impressora e [**\_ informações \_ 5**](printer-info-5.md) da impressora.</span><span class="sxs-lookup"><span data-stu-id="06a91-152">Valid values are 1, 2, 4, and 5, which correspond to the [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), and [**PRINTER\_INFO\_5**](printer-info-5.md) data structures.</span></span>

<span data-ttu-id="06a91-153">Esse valor pode ser 1, 2, 4 ou 5.</span><span class="sxs-lookup"><span data-stu-id="06a91-153">This value can be 1, 2, 4, or 5.</span></span>

</dd> <dt>

<span data-ttu-id="06a91-154">*pPrinterEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="06a91-154">*pPrinterEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06a91-155">Um ponteiro para um buffer que recebe uma matriz de [**informações de impressora \_ \_ 1**](printer-info-1.md), [**informações da impressora \_ \_ 2**](printer-info-2.md), [**informações da impressora \_ \_ 4**](printer-info-4.md)ou estruturas de [**informações da impressora \_ \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="06a91-155">A pointer to a buffer that receives an array of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span> <span data-ttu-id="06a91-156">Cada estrutura contém dados que descrevem um objeto de impressão disponível.</span><span class="sxs-lookup"><span data-stu-id="06a91-156">Each structure contains data that describes an available print object.</span></span>

<span data-ttu-id="06a91-157">Se o *nível* for 1, a matriz conterá estruturas de [**informações de impressora \_ \_ 1**](printer-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="06a91-157">If *Level* is 1, the array contains [**PRINTER\_INFO\_1**](printer-info-1.md) structures.</span></span> <span data-ttu-id="06a91-158">Se o *nível* for 2, a matriz conterá estruturas de [**informações da impressora \_ \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="06a91-158">If *Level* is 2, the array contains [**PRINTER\_INFO\_2**](printer-info-2.md) structures.</span></span> <span data-ttu-id="06a91-159">Se o *nível* for 4, a matriz conterá as estruturas de [**informações da impressora \_ \_ 4**](printer-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="06a91-159">If *Level* is 4, the array contains [**PRINTER\_INFO\_4**](printer-info-4.md) structures.</span></span> <span data-ttu-id="06a91-160">Se o *nível* for 5, a matriz conterá estruturas de [**informações da impressora \_ \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="06a91-160">If *Level* is 5, the array contains [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span>

<span data-ttu-id="06a91-161">O buffer deve ser grande o suficiente para receber a matriz de estruturas de dados e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam.</span><span class="sxs-lookup"><span data-stu-id="06a91-161">The buffer must be large enough to receive the array of data structures and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="06a91-162">Se o buffer for muito pequeno, o parâmetro *pcbNeeded* retornará o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="06a91-162">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="06a91-163">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06a91-163">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a91-164">O tamanho, em bytes, do buffer apontado por *pPrinterEnum*.</span><span class="sxs-lookup"><span data-stu-id="06a91-164">The size, in bytes, of the buffer pointed to by *pPrinterEnum*.</span></span>

</dd> <dt>

<span data-ttu-id="06a91-165">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="06a91-165">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06a91-166">Um ponteiro para um valor que recebe o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="06a91-166">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="06a91-167">*pcReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="06a91-167">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06a91-168">Um ponteiro para um valor que recebe o número de estruturas informações da impressora [**\_ \_ 1**](printer-info-1.md), [**informações da impressora \_ \_ 2**](printer-info-2.md) , [**informações da impressora \_ \_ 4**](printer-info-4.md)ou [**informações da impressora \_ \_ 5**](printer-info-5.md) que a função retorna na matriz para a qual *pPrinterEnum* aponta.</span><span class="sxs-lookup"><span data-stu-id="06a91-168">A pointer to a value that receives the number of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures that the function returns in the array to which *pPrinterEnum* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06a91-169">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06a91-169">Return value</span></span>

<span data-ttu-id="06a91-170">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="06a91-170">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="06a91-171">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="06a91-171">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a91-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="06a91-172">Remarks</span></span>

<span data-ttu-id="06a91-173">Não chame esse método em [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="06a91-173">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="06a91-174">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="06a91-174">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="06a91-175">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06a91-175">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="06a91-176">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="06a91-176">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="06a91-177">Se **EnumPrinters** retornar uma estrutura de [**informações de impressora \_ \_ 1**](printer-info-1.md) na \_ qual \_ o contêiner de enumeração de impressora é especificado, isso indica que há uma hierarquia de objetos de impressora.</span><span class="sxs-lookup"><span data-stu-id="06a91-177">If **EnumPrinters** returns a [**PRINTER\_INFO\_1**](printer-info-1.md) structure in which PRINTER\_ENUM\_CONTAINER is specified, this indicates that there is a hierarchy of printer objects.</span></span> <span data-ttu-id="06a91-178">Um aplicativo pode enumerar a hierarquia chamando **EnumPrinters** novamente, definindo o *nome* como o valor do membro **pname** da estrutura **\_ info \_ -Printer** .</span><span class="sxs-lookup"><span data-stu-id="06a91-178">An application can enumerate the hierarchy by calling **EnumPrinters** again, setting *Name* to the value of the **PRINTER\_INFO\_1** structure's **pName** member.</span></span>

<span data-ttu-id="06a91-179">A função **EnumPrinters** não recupera informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="06a91-179">The **EnumPrinters** function does not retrieve security information.</span></span> <span data-ttu-id="06a91-180">Se as estruturas de [**informações da impressora \_ \_ 2**](printer-info-2.md) forem retornadas na matriz apontada por *pPrinterEnum*, seus membros *pSecurityDescriptor* serão definidos como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="06a91-180">If [**PRINTER\_INFO\_2**](printer-info-2.md) structures are returned in the array pointed to by *pPrinterEnum*, their *pSecurityDescriptor* members will be set to **NULL**.</span></span>

<span data-ttu-id="06a91-181">Para obter informações sobre a impressora padrão, chame [**GetDefaultPrinter**](getdefaultprinter.md).</span><span class="sxs-lookup"><span data-stu-id="06a91-181">To get information about the default printer, call [**GetDefaultPrinter**](getdefaultprinter.md).</span></span>

<span data-ttu-id="06a91-182">A [**estrutura \_ informações \_ da impressora 4**](printer-info-4.md) fornece uma maneira fácil e rápida de recuperar os nomes das impressoras instaladas em um computador local, bem como as conexões remotas que um usuário estabeleceu.</span><span class="sxs-lookup"><span data-stu-id="06a91-182">The [**PRINTER\_INFO\_4**](printer-info-4.md) structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="06a91-183">Quando **EnumPrinters** é chamado com uma estrutura de dados de **informações de impressora \_ \_ 4** , essa função consulta o registro para obter as informações especificadas e retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="06a91-183">When **EnumPrinters** is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="06a91-184">Isso difere do comportamento de **EnumPrinters** quando chamado com outros níveis de **informações de \_ impressora \_ \* *_ estruturas de dados. Em particular, quando _* EnumPrinters** é chamado com uma estrutura de dados de nível 2 ([**informações da impressora \_ \_ 2**](printer-info-2.md)), ele executa uma chamada [**OpenPrinter**](openprinter.md) em cada conexão remota.</span><span class="sxs-lookup"><span data-stu-id="06a91-184">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_\**_ data structures. In particular, when _\* EnumPrinters*\* is called with a level 2 ([**PRINTER\_INFO\_2**](printer-info-2.md)) data structure, it performs an [**OpenPrinter**](openprinter.md) call on each remote connection.</span></span> <span data-ttu-id="06a91-185">Se uma conexão remota estiver inativa, ou o servidor remoto não existir mais, ou se a impressora remota não existir mais, a função deverá aguardar até que o RPC expire e, consequentemente, falhar na chamada **OpenPrinter** .</span><span class="sxs-lookup"><span data-stu-id="06a91-185">If a remote connection is down, or the remote server no longer exists, or the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="06a91-186">Isso pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="06a91-186">This can take a while.</span></span> <span data-ttu-id="06a91-187">Passar uma estrutura de **\_ informações sobre a impressora \_ 4** permite que um aplicativo recupere um mínimo de informações necessárias. se forem desejadas informações mais detalhadas, uma chamada subsequente de **EnumPrinters** nível 2 poderá ser feita.</span><span class="sxs-lookup"><span data-stu-id="06a91-187">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinters** level 2 call can be made.</span></span>

<span data-ttu-id="06a91-188">**Windows Vista:** Os dados de impressora retornados por **EnumPrinters** são recuperados de um cache local quando o valor de *Level* é 4.</span><span class="sxs-lookup"><span data-stu-id="06a91-188">**Windows Vista:** The printer data returned by **EnumPrinters** is retrieved from a local cache when the value of *Level* is 4.</span></span>

<span data-ttu-id="06a91-189">A tabela a seguir mostra a saída **EnumPrinters** para vários valores de *sinalizadores* quando o parâmetro *Level* é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="06a91-189">The following table shows the **EnumPrinters** output for various *Flags* values when the *Level* parameter is set to 1.</span></span>

<span data-ttu-id="06a91-190">Na coluna parâmetro de *nome* da tabela, você deve substituir um nome apropriado para o provedor de impressão, o domínio e a máquina.</span><span class="sxs-lookup"><span data-stu-id="06a91-190">In the *Name* parameter column of the table, you should substitute an appropriate name for Print Provider, Domain, and Machine.</span></span> <span data-ttu-id="06a91-191">Por exemplo, para "provedor de impressão", você pode usar o nome do provedor de impressão de rede ou o nome do provedor de impressão local.</span><span class="sxs-lookup"><span data-stu-id="06a91-191">For example, for "Print Provider," you could use the name of the network print provider or the name of the local print provider.</span></span> <span data-ttu-id="06a91-192">Para recuperar nomes de provedor de impressão, chame **EnumPrinters** com o *nome* definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="06a91-192">To retrieve print provider names, call **EnumPrinters** with *Name* set to **NULL**.</span></span>



| <span data-ttu-id="06a91-193">Parâmetro *flags*</span><span class="sxs-lookup"><span data-stu-id="06a91-193">*Flags* parameter</span></span>                                  | <span data-ttu-id="06a91-194">Parâmetro de *nome*</span><span class="sxs-lookup"><span data-stu-id="06a91-194">*Name* parameter</span></span>                            | <span data-ttu-id="06a91-195">Resultado</span><span class="sxs-lookup"><span data-stu-id="06a91-195">Result</span></span>                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a91-196">\_ \_ Local de enumeração de impressora (e não nome de enumeração de impressora \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="06a91-196">PRINTER\_ENUM\_LOCAL (and not PRINTER\_ENUM\_NAME)</span></span> | <span data-ttu-id="06a91-197">O parâmetro *Name* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="06a91-197">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="06a91-198">Todas as impressoras locais.</span><span class="sxs-lookup"><span data-stu-id="06a91-198">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="06a91-199">\_nome da enumeração da impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-199">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="06a91-200">"Provedor de impressão"</span><span class="sxs-lookup"><span data-stu-id="06a91-200">"Print Provider"</span></span><br/>                 | <span data-ttu-id="06a91-201">Todos os nomes de domínio</span><span class="sxs-lookup"><span data-stu-id="06a91-201">All domain names</span></span><br/>                                                                       |
| <span data-ttu-id="06a91-202">\_nome da enumeração da impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-202">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="06a91-203">"Provedor de impressão! Controlador</span><span class="sxs-lookup"><span data-stu-id="06a91-203">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="06a91-204">Todas as impressoras e servidores de impressão no domínio do computador</span><span class="sxs-lookup"><span data-stu-id="06a91-204">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="06a91-205">\_nome da enumeração da impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-205">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="06a91-206">"Provedor de impressão!! \\ \\ Tradução</span><span class="sxs-lookup"><span data-stu-id="06a91-206">"Print Provider!!\\\\Machine"</span></span><br/>    | <span data-ttu-id="06a91-207">Todas as impressoras compartilhadas na \\ \\ máquina</span><span class="sxs-lookup"><span data-stu-id="06a91-207">All printers shared at \\\\Machine</span></span><br/>                                                     |
| <span data-ttu-id="06a91-208">\_nome da enumeração da impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-208">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="06a91-209">Uma cadeia de caracteres vazia, ""</span><span class="sxs-lookup"><span data-stu-id="06a91-209">An empty string, ""</span></span><br/>              | <span data-ttu-id="06a91-210">Todas as impressoras locais.</span><span class="sxs-lookup"><span data-stu-id="06a91-210">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="06a91-211">\_nome da enumeração da impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-211">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="06a91-212">**NULL**</span><span class="sxs-lookup"><span data-stu-id="06a91-212">**NULL**</span></span><br/>                         | <span data-ttu-id="06a91-213">Todos os provedores de impressão no domínio do computador</span><span class="sxs-lookup"><span data-stu-id="06a91-213">All print providers in the computer's domain</span></span><br/>                                           |
| <span data-ttu-id="06a91-214">\_conexões de enum de impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-214">PRINTER\_ENUM\_CONNECTIONS</span></span>                         | <span data-ttu-id="06a91-215">O parâmetro *Name* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="06a91-215">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="06a91-216">Todas as impressoras remotas conectadas</span><span class="sxs-lookup"><span data-stu-id="06a91-216">All connected remote printers</span></span><br/>                                                          |
| <span data-ttu-id="06a91-217">\_rede de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-217">PRINTER\_ENUM\_NETWORK</span></span>                             | <span data-ttu-id="06a91-218">O parâmetro *Name* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="06a91-218">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="06a91-219">Todas as impressoras no domínio do computador</span><span class="sxs-lookup"><span data-stu-id="06a91-219">All printers in the computer's domain</span></span><br/>                                                  |
| <span data-ttu-id="06a91-220">\_remoto de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-220">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="06a91-221">Uma cadeia de caracteres vazia, ""</span><span class="sxs-lookup"><span data-stu-id="06a91-221">An empty string, ""</span></span><br/>              | <span data-ttu-id="06a91-222">Todas as impressoras e servidores de impressão no domínio do computador</span><span class="sxs-lookup"><span data-stu-id="06a91-222">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="06a91-223">\_remoto de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-223">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="06a91-224">"Provedor de impressão"</span><span class="sxs-lookup"><span data-stu-id="06a91-224">"Print Provider"</span></span><br/>                 | <span data-ttu-id="06a91-225">Igual ao \_ nome de enumeração da impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-225">Same as PRINTER\_ENUM\_NAME</span></span><br/>                                                            |
| <span data-ttu-id="06a91-226">\_remoto de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="06a91-226">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="06a91-227">"Provedor de impressão! Controlador</span><span class="sxs-lookup"><span data-stu-id="06a91-227">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="06a91-228">Todas as impressoras e servidores de impressão no domínio do computador, independentemente do *domínio* especificado.</span><span class="sxs-lookup"><span data-stu-id="06a91-228">All printers and print servers in computer's domain, regardless of *Domain* specified.</span></span><br/> |
| <span data-ttu-id="06a91-229">Categoria de enumeração de impressora \_ \_ \_ 3D</span><span class="sxs-lookup"><span data-stu-id="06a91-229">PRINTER\_ENUM\_CATEGORY\_3D</span></span>                        | <span data-ttu-id="06a91-230">O parâmetro *Name* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="06a91-230">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="06a91-231">Somente as impressoras 3D são enumeradas.</span><span class="sxs-lookup"><span data-stu-id="06a91-231">Only 3D printers are enumerated.</span></span><br/>                                                       |
| <span data-ttu-id="06a91-232">Categoria de enumeração de impressora \_ \_ \_ todos</span><span class="sxs-lookup"><span data-stu-id="06a91-232">PRINTER\_ENUM\_CATEGORY\_ALL</span></span>                       | <span data-ttu-id="06a91-233">O parâmetro *Name* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="06a91-233">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="06a91-234">as impressoras 3D são enumeradas, junto com todas as outras impressoras.</span><span class="sxs-lookup"><span data-stu-id="06a91-234">3D printers are enumerated, along with all other printers.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="06a91-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06a91-235">Requirements</span></span>



| <span data-ttu-id="06a91-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="06a91-236">Requirement</span></span> | <span data-ttu-id="06a91-237">Valor</span><span class="sxs-lookup"><span data-stu-id="06a91-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a91-238">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06a91-238">Minimum supported client</span></span><br/> | <span data-ttu-id="06a91-239">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06a91-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="06a91-240">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06a91-240">Minimum supported server</span></span><br/> | <span data-ttu-id="06a91-241">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06a91-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="06a91-242">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="06a91-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="06a91-243"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-243"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="06a91-244">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06a91-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="06a91-245"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-245"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="06a91-246">DLL</span><span class="sxs-lookup"><span data-stu-id="06a91-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06a91-247"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="06a91-247"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="06a91-248">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="06a91-248">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="06a91-249">**EnumPrintersW** (Unicode) e **EnumPrintersA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="06a91-249">**EnumPrintersW** (Unicode) and **EnumPrintersA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="06a91-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="06a91-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a91-251">Impressão</span><span class="sxs-lookup"><span data-stu-id="06a91-251">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="06a91-252">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="06a91-252">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="06a91-253">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="06a91-253">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="06a91-254">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="06a91-254">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="06a91-255">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="06a91-255">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="06a91-256">**Informações da impressora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="06a91-256">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="06a91-257">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="06a91-257">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="06a91-258">**Informações da impressora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="06a91-258">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="06a91-259">**Informações da impressora \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="06a91-259">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="06a91-260">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="06a91-260">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

