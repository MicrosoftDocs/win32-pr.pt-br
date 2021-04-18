---
description: A função getprinter recupera informações sobre uma impressora especificada.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: Função getprinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784646"
---
# <a name="getprinter-function"></a><span data-ttu-id="96d1f-103">Função getprinter</span><span class="sxs-lookup"><span data-stu-id="96d1f-103">GetPrinter function</span></span>

<span data-ttu-id="96d1f-104">A função **Getprinter** recupera informações sobre uma impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="96d1f-104">The **GetPrinter** function retrieves information about a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96d1f-105">Syntax</span></span>


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="96d1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96d1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d1f-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96d1f-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d1f-108">Um identificador para a impressora para a qual a função recupera informações.</span><span class="sxs-lookup"><span data-stu-id="96d1f-108">A handle to the printer for which the function retrieves information.</span></span> <span data-ttu-id="96d1f-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="96d1f-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="96d1f-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="96d1f-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d1f-111">O nível ou tipo de estrutura que a função armazena no buffer apontado por *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="96d1f-111">The level or type of structure that the function stores into the buffer pointed to by *pPrinter*.</span></span>

<span data-ttu-id="96d1f-112">Esse valor pode ser 1, 2, 3, 4, 5, 6, 7, 8 ou 9.</span><span class="sxs-lookup"><span data-stu-id="96d1f-112">This value can be 1, 2, 3, 4, 5, 6, 7, 8 or 9.</span></span>

</dd> <dt>

<span data-ttu-id="96d1f-113">*pPrinter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="96d1f-113">*pPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96d1f-114">Um ponteiro para um buffer que recebe uma estrutura que contém informações sobre a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="96d1f-114">A pointer to a buffer that receives a structure containing information about the specified printer.</span></span> <span data-ttu-id="96d1f-115">O buffer deve ser grande o suficiente para receber a estrutura e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam.</span><span class="sxs-lookup"><span data-stu-id="96d1f-115">The buffer must be large enough to receive the structure and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="96d1f-116">Se o buffer for muito pequeno, o parâmetro *pcbNeeded* retornará o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="96d1f-116">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

<span data-ttu-id="96d1f-117">O tipo de estrutura é determinado pelo valor do *nível*.</span><span class="sxs-lookup"><span data-stu-id="96d1f-117">The type of structure is determined by the value of *Level*.</span></span>



| <span data-ttu-id="96d1f-118">Nível</span><span class="sxs-lookup"><span data-stu-id="96d1f-118">Level</span></span>                                                                                                | <span data-ttu-id="96d1f-119">Estrutura</span><span class="sxs-lookup"><span data-stu-id="96d1f-119">Structure</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="96d1f-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-120"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="96d1f-121">Uma estrutura de [**informações da impressora \_ \_ 1**](printer-info-1.md) que contém informações gerais sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="96d1f-121">A [**PRINTER\_INFO\_1**](printer-info-1.md) structure containing general printer information.</span></span><br/>                                                                                                        |
| <span id="2"></span><dl> <span data-ttu-id="96d1f-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-122"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="96d1f-123">Uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) que contém informações detalhadas sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="96d1f-123">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                             |
| <span id="3"></span><dl> <span data-ttu-id="96d1f-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="96d1f-125">Uma estrutura de [**informações da impressora \_ \_ 3**](printer-info-3.md) que contém as informações de segurança da impressora.</span><span class="sxs-lookup"><span data-stu-id="96d1f-125">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                 |
| <span id="4"></span><dl> <span data-ttu-id="96d1f-126"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="96d1f-127">Uma estrutura de [**informações da impressora \_ \_ 4**](printer-info-4.md) que contém informações de impressora mínimas, incluindo o nome da impressora, o nome do servidor e se a impressora é remota ou local.</span><span class="sxs-lookup"><span data-stu-id="96d1f-127">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="96d1f-128"><dt>**05**</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-128"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="96d1f-129">Uma estrutura de [**informações da impressora \_ \_ 5**](printer-info-5.md) que contém informações de impressora, como atributos de impressora e configurações de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="96d1f-129">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                               |
| <span id="6"></span><dl> <span data-ttu-id="96d1f-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-130"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="96d1f-131">Uma estrutura de [**informações da impressora \_ \_ 6**](printer-info-6.md) especificando o valor de status de uma impressora.</span><span class="sxs-lookup"><span data-stu-id="96d1f-131">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                      |
| <span id="7"></span><dl> <span data-ttu-id="96d1f-132"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-132"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="96d1f-133">Uma estrutura de [**informações da impressora \_ \_ 7**](printer-info-7.md) que indica se a impressora está publicada no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="96d1f-133">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure that indicates whether the printer is published in the directory service.</span></span><br/>                                                                      |
| <span id="8"></span><dl> <span data-ttu-id="96d1f-134"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-134"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="96d1f-135">Uma estrutura de [**informações da impressora \_ \_ 8**](printer-info-8.md) especificando as configurações de impressora padrão globais.</span><span class="sxs-lookup"><span data-stu-id="96d1f-135">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                |
| <span id="9"></span><dl> <span data-ttu-id="96d1f-136"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-136"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="96d1f-137">Uma estrutura de [**informações da impressora \_ \_ 9**](printer-info-9.md) especificando as configurações de impressora padrão por usuário.</span><span class="sxs-lookup"><span data-stu-id="96d1f-137">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="96d1f-138">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96d1f-138">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d1f-139">O tamanho, em bytes, do buffer apontado por *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="96d1f-139">The size, in bytes, of the buffer pointed to by *pPrinter*.</span></span>

</dd> <dt>

<span data-ttu-id="96d1f-140">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="96d1f-140">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96d1f-141">Um ponteiro para uma variável que a função define para o tamanho, em bytes, das informações da impressora.</span><span class="sxs-lookup"><span data-stu-id="96d1f-141">A pointer to a variable that the function sets to the size, in bytes, of the printer information.</span></span> <span data-ttu-id="96d1f-142">Se *cbBuf* for menor que esse valor, **getprinter** falhará e o valor representará o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="96d1f-142">If *cbBuf* is smaller than this value, **GetPrinter** fails, and the value represents the required buffer size.</span></span> <span data-ttu-id="96d1f-143">Se *cbBuf* for igual a ou maior que esse valor, **getprinter** terá sucesso e o valor representará o número de bytes armazenados no buffer.</span><span class="sxs-lookup"><span data-stu-id="96d1f-143">If *cbBuf* is equal to or greater than this value, **GetPrinter** succeeds, and the value represents the number of bytes stored in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d1f-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96d1f-144">Return value</span></span>

<span data-ttu-id="96d1f-145">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="96d1f-145">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="96d1f-146">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="96d1f-146">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="96d1f-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="96d1f-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="96d1f-148">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="96d1f-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="96d1f-149">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96d1f-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="96d1f-150">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="96d1f-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="96d1f-151">O membro **pDevMode** nas estruturas [**\_ info \_ 2**](printer-info-2.md), [**Printer \_ info \_ 8**](printer-info-8.md)e [**Printer \_ info \_ 9**](printer-info-9.md) da impressora pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="96d1f-151">The **pDevMode** member in the [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_8**](printer-info-8.md), and [**PRINTER\_INFO\_9**](printer-info-9.md) structures can be **NULL**.</span></span> <span data-ttu-id="96d1f-152">Quando isso acontecer, a impressora ficará inutilizável até que o driver seja reinstalado com êxito.</span><span class="sxs-lookup"><span data-stu-id="96d1f-152">When this happens, the printer is unusable until the driver is reinstalled successfully.</span></span>

<span data-ttu-id="96d1f-153">Para as [**estruturas \_ informações \_ da impressora 2**](printer-info-2.md) e [**informações da impressora \_ \_ 3**](printer-info-3.md) que contêm um ponteiro para um descritor de segurança, a função recupera somente os componentes do descritor de segurança que o chamador tem permissão para ler.</span><span class="sxs-lookup"><span data-stu-id="96d1f-153">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function retrieves only those components of the security descriptor that the caller has permission to read.</span></span> <span data-ttu-id="96d1f-154">Para recuperar componentes específicos do descritor de segurança, você deve especificar os direitos de acesso necessários ao chamar a função [**OpenPrinter**](openprinter.md) para recuperar um identificador para a impressora.</span><span class="sxs-lookup"><span data-stu-id="96d1f-154">To retrieve particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="96d1f-155">A tabela a seguir mostra os direitos de acesso necessários para ler os vários componentes do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="96d1f-155">The following table shows the access rights required to read the various security descriptor components.</span></span>



| <span data-ttu-id="96d1f-156">Direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="96d1f-156">Access Right</span></span>                        | <span data-ttu-id="96d1f-157">Componente de descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="96d1f-157">Security Descriptor Component</span></span>                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d1f-158">controle de leitura \_</span><span class="sxs-lookup"><span data-stu-id="96d1f-158">READ\_CONTROL</span></span><br/>            | <span data-ttu-id="96d1f-159">Proprietário</span><span class="sxs-lookup"><span data-stu-id="96d1f-159">Owner</span></span><br/> <span data-ttu-id="96d1f-160">Grupo primário</span><span class="sxs-lookup"><span data-stu-id="96d1f-160">Primary group</span></span><br/> <span data-ttu-id="96d1f-161">DACL (lista de controle de acesso discricionário)</span><span class="sxs-lookup"><span data-stu-id="96d1f-161">Discretionary access-control list (DACL)</span></span><br/> |
| <span data-ttu-id="96d1f-162">\_segurança do sistema de acesso \_</span><span class="sxs-lookup"><span data-stu-id="96d1f-162">ACCESS\_SYSTEM\_SECURITY</span></span><br/> | <span data-ttu-id="96d1f-163">Lista de controle de acesso (SACL) do sistema</span><span class="sxs-lookup"><span data-stu-id="96d1f-163">System access-control list (SACL)</span></span><br/>                                                  |



 

<span data-ttu-id="96d1f-164">Se você especificar nível 7, o membro **dwAction** das [**informações da impressora \_ \_ 7**](printer-info-7.md) retornará um dos seguintes valores para indicar se a impressora está publicada no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="96d1f-164">If you specify level 7, the **dwAction** member of [**PRINTER\_INFO\_7**](printer-info-7.md) returns one of the following values to indicate whether the printer is published in the directory service.</span></span>



| <span data-ttu-id="96d1f-165">valor de dwAction</span><span class="sxs-lookup"><span data-stu-id="96d1f-165">dwAction value</span></span>     | <span data-ttu-id="96d1f-166">Significado</span><span class="sxs-lookup"><span data-stu-id="96d1f-166">Meaning</span></span>                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d1f-167">publicação do DSPRINT \_</span><span class="sxs-lookup"><span data-stu-id="96d1f-167">DSPRINT\_PUBLISH</span></span>   | <span data-ttu-id="96d1f-168">A impressora é publicada.</span><span class="sxs-lookup"><span data-stu-id="96d1f-168">The printer is published.</span></span> <span data-ttu-id="96d1f-169">O membro **pszObjectGUID** contém o GUID do objeto de fila de impressão dos serviços de diretório associado à impressora.</span><span class="sxs-lookup"><span data-stu-id="96d1f-169">The **pszObjectGUID** member contains the GUID of the directory services print queue object associated with the printer.</span></span>                                                                                                       |
| <span data-ttu-id="96d1f-170">DSPRINT \_ Cancelar publicação</span><span class="sxs-lookup"><span data-stu-id="96d1f-170">DSPRINT\_UNPUBLISH</span></span> | <span data-ttu-id="96d1f-171">A impressora não está publicada.</span><span class="sxs-lookup"><span data-stu-id="96d1f-171">The printer is not published.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="96d1f-172">DSPRINT \_ pendente</span><span class="sxs-lookup"><span data-stu-id="96d1f-172">DSPRINT\_PENDING</span></span>   | <span data-ttu-id="96d1f-173">Indica que o sistema está tentando concluir uma operação de publicação ou cancelamento de publicação.</span><span class="sxs-lookup"><span data-stu-id="96d1f-173">Indicates that the system is attempting to complete a publish or unpublish operation.</span></span> <span data-ttu-id="96d1f-174">Se uma chamada [**Setprintr**](setprinter.md) falhar ao publicar ou cancelar a publicação de uma impressora, o sistema fará outras tentativas de concluir a operação em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="96d1f-174">If a [**SetPrinter**](setprinter.md) call fails to publish or unpublish a printer, the system makes further attempts to complete the operation in the background.</span></span> |



 

<span data-ttu-id="96d1f-175">A partir do Windows Vista, os dados da impressora retornados pelo **Getprinter** são recuperados de um cache local quando o *hPrinter* refere-se a uma impressora hospedada por um servidor de impressão e há pelo menos uma conexão aberta com o servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="96d1f-175">Starting with Windows Vista, the printer data returned by **GetPrinter** is retrieved from a local cache when *hPrinter* refers to a printer hosted by a print server and there is at least one open connection to the print server.</span></span> <span data-ttu-id="96d1f-176">Em todas as outras configurações, os dados da impressora são consultados do servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="96d1f-176">In all other configurations, the printer data is queried from the print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d1f-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96d1f-177">Requirements</span></span>



| <span data-ttu-id="96d1f-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d1f-178">Requirement</span></span> | <span data-ttu-id="96d1f-179">Valor</span><span class="sxs-lookup"><span data-stu-id="96d1f-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d1f-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96d1f-180">Minimum supported client</span></span><br/> | <span data-ttu-id="96d1f-181">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96d1f-181">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="96d1f-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96d1f-182">Minimum supported server</span></span><br/> | <span data-ttu-id="96d1f-183">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96d1f-183">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="96d1f-184">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96d1f-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d1f-185"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-185"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="96d1f-186">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96d1f-186">Library</span></span><br/>                  | <dl> <span data-ttu-id="96d1f-187"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-187"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="96d1f-188">DLL</span><span class="sxs-lookup"><span data-stu-id="96d1f-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96d1f-189"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="96d1f-189"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="96d1f-190">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="96d1f-190">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="96d1f-191">**GetPrinterW** (Unicode) e **getprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="96d1f-191">**GetPrinterW** (Unicode) and **GetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="96d1f-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="96d1f-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d1f-193">Impressão</span><span class="sxs-lookup"><span data-stu-id="96d1f-193">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="96d1f-194">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="96d1f-194">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="96d1f-195">**AbortPrinter**</span><span class="sxs-lookup"><span data-stu-id="96d1f-195">**AbortPrinter**</span></span>](abortprinter.md)
</dt> <dt>

[<span data-ttu-id="96d1f-196">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="96d1f-196">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="96d1f-197">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="96d1f-197">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="96d1f-198">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="96d1f-198">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="96d1f-199">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="96d1f-199">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="96d1f-200">**Informações da impressora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="96d1f-200">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="96d1f-201">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="96d1f-201">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="96d1f-202">**Informações da impressora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="96d1f-202">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="96d1f-203">**Informações da impressora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="96d1f-203">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="96d1f-204">**Informações da impressora \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="96d1f-204">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="96d1f-205">**Informações da impressora \_ \_ 7**</span><span class="sxs-lookup"><span data-stu-id="96d1f-205">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="96d1f-206">**Informações da impressora \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="96d1f-206">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="96d1f-207">**Informações da impressora \_ \_ 9**</span><span class="sxs-lookup"><span data-stu-id="96d1f-207">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="96d1f-208">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="96d1f-208">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="96d1f-209">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="96d1f-209">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




