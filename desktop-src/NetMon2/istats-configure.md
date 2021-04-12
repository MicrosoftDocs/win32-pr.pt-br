---
description: O método configure envia informações de configuração de captura.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'Método IStats:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171287"
---
# <a name="istatsconfigure-method"></a><span data-ttu-id="2ca57-103">Método IStats:: Configure</span><span class="sxs-lookup"><span data-stu-id="2ca57-103">IStats::Configure method</span></span>

<span data-ttu-id="2ca57-104">O método **Configure** envia informações de configuração de captura.</span><span class="sxs-lookup"><span data-stu-id="2ca57-104">The **Configure** method submits capture configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca57-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ca57-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="2ca57-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ca57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ca57-107">*hConfigurationBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ca57-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca57-108">Identificador para o BLOB que o chamador configura.</span><span class="sxs-lookup"><span data-stu-id="2ca57-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="2ca57-109">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2ca57-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca57-110">Identificador para um BLOB de erro que contém informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="2ca57-110">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ca57-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ca57-111">Return value</span></span>

<span data-ttu-id="2ca57-112">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="2ca57-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2ca57-113">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="2ca57-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2ca57-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2ca57-114">Return code</span></span>                                                                                                         | <span data-ttu-id="2ca57-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ca57-115">Description</span></span>                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ca57-116"><dt>**\_cadeia de blob NMERR \_ \_ inválida**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-116"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="2ca57-117">A cadeia de caracteres não é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="2ca57-117">The string is not null-terminated.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="2ca57-118"><dt>**\_blob NMERR \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-118"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="2ca57-119">O método **createBlob** não foi chamado.</span><span class="sxs-lookup"><span data-stu-id="2ca57-119">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="2ca57-120"><dt>**NMERR \_ \_ blob inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-120"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="2ca57-121">O objeto que é apontado não é um BLOB.</span><span class="sxs-lookup"><span data-stu-id="2ca57-121">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="2ca57-122"><dt>**BLOB de upNMERR de \_ nível \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-122"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="2ca57-123">O número de versão do BLOB está incorreto.</span><span class="sxs-lookup"><span data-stu-id="2ca57-123">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="2ca57-124"><dt>**a \_ entrada de blob NMERR \_ \_ já \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-124"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="2ca57-125">Já existe uma entrada de BLOB.</span><span class="sxs-lookup"><span data-stu-id="2ca57-125">A BLOB entry already exists.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="2ca57-126"><dt>**a \_ entrada de blob NMERR não \_ \_ \_ \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-126"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="2ca57-127">O BLOB de configuração especificado pelo parâmetro *hConfigurationBlob* não tem uma entrada necessária para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="2ca57-127">The configuration BLOB specified by the *hConfigurationBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="2ca57-128">Examine o BLOB de erro retornado pelo parâmetro *hErrorBlob* para determinar qual entrada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="2ca57-128">Look at the error BLOB returned by the *hErrorBlob* parameter to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="2ca57-129"><dt>**\_ \_ especificador ambíguo NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-129"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="2ca57-130">O BLOB não tem informações de proprietário ou categoria.</span><span class="sxs-lookup"><span data-stu-id="2ca57-130">The BLOB lacks owner or category information.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="2ca57-131"><dt>**\_proprietário do blob NMERR \_ \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-131"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="2ca57-132">A seção de proprietário do BLOB não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="2ca57-132">The Owner section of the BLOB was not found.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="2ca57-133"><dt>**\_categoria de blob NMERR \_ \_ não \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-133"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="2ca57-134">A seção de categoria do BLOB não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="2ca57-134">The Category section of the BLOB was not found.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="2ca57-135"><dt>**NMERR \_ \_ categoria desconhecida**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-135"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="2ca57-136">Informações de categoria foram encontradas, mas não compreendidas.</span><span class="sxs-lookup"><span data-stu-id="2ca57-136">Category information was found but not understood.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="2ca57-137"><dt>**\_marca desconhecida \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-137"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="2ca57-138">Informações de marca foram encontradas, mas não compreendidas.</span><span class="sxs-lookup"><span data-stu-id="2ca57-138">Tag information was found but not understood.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="2ca57-139"><dt>**\_erro de \_ conversão de blob NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-139"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="2ca57-140">O BLOB está corrompido.</span><span class="sxs-lookup"><span data-stu-id="2ca57-140">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="2ca57-141"><dt>**NMERR \_ \_ gatilho ilegal**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-141"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="2ca57-142">A parte do gatilho do BLOB está corrompida.</span><span class="sxs-lookup"><span data-stu-id="2ca57-142">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="2ca57-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ca57-143">Remarks</span></span>

<span data-ttu-id="2ca57-144">Você deve aplicar esse método para reiniciar um NPP que foi iniciado, interrompido, mas não desconectado.</span><span class="sxs-lookup"><span data-stu-id="2ca57-144">You must apply this method to restart an NPP that has been started, stopped but not disconnected.</span></span>

<span data-ttu-id="2ca57-145">O BLOB de erro retornado por *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de configuração especificado no parâmetro *hConfigurationBlob* .</span><span class="sxs-lookup"><span data-stu-id="2ca57-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in the *hConfigurationBlob* parameter.</span></span> <span data-ttu-id="2ca57-146">O BLOB de erro retornado contém informações de erro que o aplicativo pode usar para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="2ca57-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="2ca57-147">Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar é incluída no blob de erros retornado.</span><span class="sxs-lookup"><span data-stu-id="2ca57-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca57-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca57-148">Requirements</span></span>



| <span data-ttu-id="2ca57-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca57-149">Requirement</span></span> | <span data-ttu-id="2ca57-150">Valor</span><span class="sxs-lookup"><span data-stu-id="2ca57-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca57-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca57-151">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca57-152">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ca57-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2ca57-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca57-153">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca57-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ca57-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2ca57-155">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2ca57-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ca57-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2ca57-157">DLL</span><span class="sxs-lookup"><span data-stu-id="2ca57-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ca57-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ca57-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca57-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ca57-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca57-160">IStats</span><span class="sxs-lookup"><span data-stu-id="2ca57-160">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="2ca57-161">ISTATS:: conectar</span><span class="sxs-lookup"><span data-stu-id="2ca57-161">ISTATS::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="2ca57-162">BLOBs de Monitor de Rede</span><span class="sxs-lookup"><span data-stu-id="2ca57-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




