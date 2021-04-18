---
description: O método configure envia informações de configuração para uma captura.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'Método IESP:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780858"
---
# <a name="iespconfigure-method"></a><span data-ttu-id="f2028-103">Método IESP:: Configure</span><span class="sxs-lookup"><span data-stu-id="f2028-103">IESP::Configure method</span></span>

<span data-ttu-id="f2028-104">O método **Configure** envia informações de configuração para uma captura.</span><span class="sxs-lookup"><span data-stu-id="f2028-104">The **Configure** method submits configuration information for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2028-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2028-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="f2028-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2028-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2028-107">*hConfigurationBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2028-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2028-108">Identificador para o BLOB que o chamador configura.</span><span class="sxs-lookup"><span data-stu-id="f2028-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="f2028-109">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f2028-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2028-110">Identificador para um BLOB de erro que contém informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="f2028-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="f2028-111">Para obter informações sobre o conteúdo de um BLOB de erro, consulte a seção comentários neste tópico.</span><span class="sxs-lookup"><span data-stu-id="f2028-111">For information about the contents of an error BLOB, see the Remarks section in this topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2028-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2028-112">Return value</span></span>

<span data-ttu-id="f2028-113">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="f2028-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f2028-114">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="f2028-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f2028-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f2028-115">Return code</span></span>                                                                                                         | <span data-ttu-id="f2028-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2028-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2028-117"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-117"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>                | <span data-ttu-id="f2028-118">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="f2028-118">The NPP is not connected to the network.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="f2028-119"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>                      | <span data-ttu-id="f2028-120">O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="f2028-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="f2028-121"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-121"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                     | <span data-ttu-id="f2028-122">O NPP relata que a sessão de captura foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="f2028-122">The NPP reports that the capture session has started.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="f2028-123"><dt>**NMERR \_ \_ gatilho ilegal**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-123"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="f2028-124">A parte do gatilho do BLOB de configuração está corrompida.</span><span class="sxs-lookup"><span data-stu-id="f2028-124">The trigger portion of the configuration BLOB is corrupt.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="f2028-125"><dt>**a \_ entrada de blob NMERR não \_ \_ \_ \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-125"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="f2028-126">O BLOB de configuração especificado por *hConfigurationBlob* não tem uma entrada necessária para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="f2028-126">The configuration BLOB specified by *hConfigurationBlob* is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="f2028-127">Examine o BLOB de erro retornado por *hErrorBlob* para determinar qual entrada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="f2028-127">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="f2028-128"><dt>**\_erro de \_ conversão de blob NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-128"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="f2028-129">O BLOB está corrompido.</span><span class="sxs-lookup"><span data-stu-id="f2028-129">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="f2028-130"><dt>**\_blob NMERR \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-130"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="f2028-131">O método **createBlob** não foi chamado.</span><span class="sxs-lookup"><span data-stu-id="f2028-131">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="f2028-132"><dt>**NMERR \_ \_ blob inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-132"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="f2028-133">O objeto que é apontado não é um BLOB.</span><span class="sxs-lookup"><span data-stu-id="f2028-133">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="f2028-134"><dt>**\_cadeia de blob NMERR \_ \_ inválida**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-134"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="f2028-135">A cadeia de caracteres não é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="f2028-135">The string is not null-terminated.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="f2028-136"><dt>**BLOB de upNMERR de \_ nível \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-136"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="f2028-137">O número de versão do BLOB está incorreto.</span><span class="sxs-lookup"><span data-stu-id="f2028-137">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="f2028-138"><dt>**NMERR \_ \_ de \_ memória insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-138"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="f2028-139">Não havia memória disponível.</span><span class="sxs-lookup"><span data-stu-id="f2028-139">No memory was available.</span></span> <span data-ttu-id="f2028-140">Desligue o Windows para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="f2028-140">Shut down windows to free up resources.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="f2028-141"><dt>**\_tempo limite de NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-141"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="f2028-142">O tempo limite da solicitação foi atingido.</span><span class="sxs-lookup"><span data-stu-id="f2028-142">The request has timed out.</span></span><br/>                                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="f2028-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2028-143">Remarks</span></span>

<span data-ttu-id="f2028-144">Você deve aplicar esse método para reiniciar um NPP que foi iniciado e interrompido, mas não desconectado.</span><span class="sxs-lookup"><span data-stu-id="f2028-144">You must apply this method to restart an NPP that has been started and stopped, but not disconnected.</span></span>

<span data-ttu-id="f2028-145">O BLOB de erro retornado pelo parâmetro *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de configuração especificado em *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="f2028-145">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="f2028-146">O BLOB de erro retornado contém informações de erro que o aplicativo pode usar para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="f2028-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="f2028-147">Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar é incluída no blob de erros retornado.</span><span class="sxs-lookup"><span data-stu-id="f2028-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2028-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2028-148">Requirements</span></span>



| <span data-ttu-id="f2028-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2028-149">Requirement</span></span> | <span data-ttu-id="f2028-150">Valor</span><span class="sxs-lookup"><span data-stu-id="f2028-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2028-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2028-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f2028-152">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f2028-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f2028-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2028-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f2028-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f2028-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f2028-155">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f2028-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2028-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f2028-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f2028-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2028-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2028-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

 




