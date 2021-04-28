---
description: 'Método IStats:: Connect – o método Connect conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração para a conexão.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'Método IStats:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0719b6ff56aaa8c0be02f86d62ac23d4003aa3d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098474"
---
# <a name="istatsconnect-method"></a><span data-ttu-id="8144f-103">Método IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="8144f-103">IStats::Connect method</span></span>

<span data-ttu-id="8144f-104">O método **Connect** conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração para a conexão.</span><span class="sxs-lookup"><span data-stu-id="8144f-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8144f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8144f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="8144f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8144f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8144f-107">*hInputBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8144f-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8144f-108">Identificador para o BLOB que especifica a NIC à qual o NPP se conecta e as informações de configuração para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="8144f-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="8144f-109">*StatusCallbackProc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8144f-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8144f-110">Endereço da função de retorno de chamada do usuário, que recebe atualizações de status, como gatilhos.</span><span class="sxs-lookup"><span data-stu-id="8144f-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="8144f-111">Se uma função de retorno de chamada não for usada, defina esse parâmetro e o parâmetro *userContext* como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8144f-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8144f-112">*UserContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8144f-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8144f-113">Valor passado quando a função de retorno de chamada do usuário é chamada.</span><span class="sxs-lookup"><span data-stu-id="8144f-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="8144f-114">O valor desse parâmetro é normalmente o HWND ou um ponteiro ' this '.</span><span class="sxs-lookup"><span data-stu-id="8144f-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="8144f-115">Se uma função de retorno de chamada não for especificada, defina esse parâmetro e o parâmetro *StatusCallbackProc* como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8144f-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8144f-116">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8144f-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8144f-117">Identificador para um BLOB de erro que contém informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="8144f-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8144f-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8144f-118">Return value</span></span>

<span data-ttu-id="8144f-119">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="8144f-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8144f-120">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro (que incluem os erros retornados pela chamada interna **IStats:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="8144f-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IStats::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8144f-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8144f-121">Return code</span></span></th>
<th><span data-ttu-id="8144f-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="8144f-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="8144f-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-124">Esta instância do objeto COM NPP já está conectada à rede.</span><span class="sxs-lookup"><span data-stu-id="8144f-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8144f-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-126">O BLOB de configuração está corrompido.</span><span class="sxs-lookup"><span data-stu-id="8144f-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="8144f-127">Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8144f-127">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8144f-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-129">O BLOB de entrada especificado pelo parâmetro <em>hInputBlob</em> não tem uma entrada necessária para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="8144f-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="8144f-130">Esse erro pode ser gerado pela chamada <strong>IStats:: Connect</strong> ou <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8144f-130">This error might be generated by the <strong>IStats::Connect</strong> or <strong>IStats::Configure</strong> call.</span></span> <span data-ttu-id="8144f-131">Examine o BLOB de erro retornado por <em>hErrorBlob</em> para determinar qual entrada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="8144f-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8144f-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-133">A função <strong>createBlob</strong> não foi chamada.</span><span class="sxs-lookup"><span data-stu-id="8144f-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="8144f-134">Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8144f-134">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8144f-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-136">A cadeia de caracteres não é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="8144f-136">The string is not null-terminated.</span></span> <span data-ttu-id="8144f-137">Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8144f-137">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8144f-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-139">A parte do gatilho do BLOB de entrada está corrompida.</span><span class="sxs-lookup"><span data-stu-id="8144f-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="8144f-140">Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8144f-140">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8144f-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-142">O objeto especificado em <em>hInputBlob</em> não é um blob.</span><span class="sxs-lookup"><span data-stu-id="8144f-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="8144f-143">Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8144f-143">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8144f-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-145">O diretório de captura padrão não foi definido no registro.</span><span class="sxs-lookup"><span data-stu-id="8144f-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="8144f-146">Para definir o diretório de captura, use o caminho a seguir.</span><span class="sxs-lookup"><span data-stu-id="8144f-146">To set the capture directory, use the following path.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8144f-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-148">A memória necessária para executar esta operação não estava disponível.</span><span class="sxs-lookup"><span data-stu-id="8144f-148">The memory required to perform this operation was unavailable.</span></span> <span data-ttu-id="8144f-149">Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8144f-149">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8144f-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-151">O tempo limite da solicitação foi atingido. Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8144f-151">The request has timed out. This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8144f-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8144f-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8144f-153">O número de versão do BLOB especificado em <em>hInputBlob</em> está incorreto.</span><span class="sxs-lookup"><span data-stu-id="8144f-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="8144f-154">Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8144f-154">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8144f-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="8144f-155">Remarks</span></span>

<span data-ttu-id="8144f-156">Quando o método **Connect** é chamado, monitor de rede chama automaticamente o método **IStats:: Configure** usando o blob fornecido pelo parâmetro *hInputBlob* .</span><span class="sxs-lookup"><span data-stu-id="8144f-156">When the **Connect** method is called, Network Monitor automatically calls the **IStats::Configure** method by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="8144f-157">Observe que todos os códigos de erro retornados pela chamada para **IStats:: Configure** são passados de volta e retornados pela chamada **IStats:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="8144f-157">Note that any error codes returned by the call to **IStats::Configure** are passed back and returned by the **IStats::Connect** call.</span></span>

<span data-ttu-id="8144f-158">Esse método deve ser chamado antes que você possa iniciar a captura de quadros.</span><span class="sxs-lookup"><span data-stu-id="8144f-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="8144f-159">Observe que quando você se conecta à rede usando esse método, você deve continuar a usar a interface **IStats** para capturar quadros.</span><span class="sxs-lookup"><span data-stu-id="8144f-159">Note that when you connect to the network by using this method, you must continue to use the **IStats** interface to capture frames.</span></span>

<span data-ttu-id="8144f-160">O BLOB de entrada especificado por *hInputBlob* pode ser obtido chamando os métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable** .</span><span class="sxs-lookup"><span data-stu-id="8144f-160">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="8144f-161">O BLOB de erro retornado pelo parâmetro *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de entrada especificado em *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="8144f-161">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="8144f-162">O BLOB de erro retornado contém informações de erro que o aplicativo pode usar para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="8144f-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="8144f-163">Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada que monitor de rede não pôde localizar será incluída no blob de erros retornado.</span><span class="sxs-lookup"><span data-stu-id="8144f-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="8144f-164">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="8144f-164">For information about</span></span>                                             | <span data-ttu-id="8144f-165">Consulte</span><span class="sxs-lookup"><span data-stu-id="8144f-165">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8144f-166">Obtendo o BLOB de entrada que representa uma placa de interface de rede</span><span class="sxs-lookup"><span data-stu-id="8144f-166">Obtaining the input BLOB that represents a network interface card</span></span> | [<span data-ttu-id="8144f-167">Selecionando uma placa de interface de rede</span><span class="sxs-lookup"><span data-stu-id="8144f-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="8144f-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8144f-168">Requirements</span></span>



| <span data-ttu-id="8144f-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="8144f-169">Requirement</span></span> | <span data-ttu-id="8144f-170">Valor</span><span class="sxs-lookup"><span data-stu-id="8144f-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8144f-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8144f-171">Minimum supported client</span></span><br/> | <span data-ttu-id="8144f-172">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8144f-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8144f-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8144f-173">Minimum supported server</span></span><br/> | <span data-ttu-id="8144f-174">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8144f-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8144f-175">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8144f-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="8144f-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8144f-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8144f-177">DLL</span><span class="sxs-lookup"><span data-stu-id="8144f-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8144f-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8144f-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8144f-179">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8144f-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8144f-180">IStats</span><span class="sxs-lookup"><span data-stu-id="8144f-180">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="8144f-181">IStats:: configurar</span><span class="sxs-lookup"><span data-stu-id="8144f-181">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="8144f-182">IStats::D isconnect</span><span class="sxs-lookup"><span data-stu-id="8144f-182">IStats::Disconnect</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="8144f-183">BLOBs de Monitor de Rede</span><span class="sxs-lookup"><span data-stu-id="8144f-183">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




