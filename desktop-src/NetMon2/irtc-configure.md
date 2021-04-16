---
description: Envia dados de configuração para uma captura de dados.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'Método IRTC:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751170"
---
# <a name="irtcconfigure-method"></a><span data-ttu-id="e0b9d-103">Método IRTC:: Configure</span><span class="sxs-lookup"><span data-stu-id="e0b9d-103">IRTC::Configure method</span></span>

<span data-ttu-id="e0b9d-104">O método [**Configure**](configure.md) envia dados de configuração para uma captura de dados.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-104">The [**Configure**](configure.md) method submits configuration data for a data capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b9d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0b9d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="e0b9d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0b9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b9d-107">*hConfigurationBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0b9d-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b9d-108">Um identificador para o BLOB que é configurado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-108">A handle to the BLOB that is configured by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="e0b9d-109">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0b9d-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b9d-110">Um identificador para um BLOB de erro que contém dados de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-110">A handle to an error BLOB that contains additional error data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b9d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0b9d-111">Return value</span></span>

<span data-ttu-id="e0b9d-112">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e0b9d-113">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="e0b9d-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e0b9d-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e0b9d-114">Return code</span></span>                                                                                                         | <span data-ttu-id="e0b9d-115">Description</span><span class="sxs-lookup"><span data-stu-id="e0b9d-115">Description</span></span>                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0b9d-116"><dt>**\_blob NMERR \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-116"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="e0b9d-117">O método **createBlob** não foi chamado.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-117">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                 |
| <dl> <span data-ttu-id="e0b9d-118"><dt>**NMERR \_ \_ blob inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-118"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="e0b9d-119">O objeto apontado não é um BLOB.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-119">The object pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="e0b9d-120"><dt>**BLOB de upNMERR de \_ nível \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-120"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="e0b9d-121">O número de versão do BLOB está incorreto.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-121">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="e0b9d-122"><dt>**a \_ entrada de blob NMERR \_ \_ já \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-122"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="e0b9d-123">Duplicar BLOB.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-123">Duplicate BLOB.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="e0b9d-124"><dt>**a \_ entrada de blob NMERR não \_ \_ \_ \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-124"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="e0b9d-125">O BLOB de configuração especificado por *hConfigurationBlob* não tem uma entrada necessária para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-125">The configuration BLOB specified by *hConfigurationBlob* lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="e0b9d-126">Exiba o BLOB de erro retornado por *hErrorBlob* para determinar qual entrada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-126">View the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="e0b9d-127"><dt>**\_ \_ especificador ambíguo NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-127"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="e0b9d-128">O proprietário do BLOB ou os dados da categoria estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-128">The BLOB Owner or Category data is missing.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="e0b9d-129"><dt>**\_proprietário do blob NMERR \_ \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-129"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="e0b9d-130">A seção de proprietário do BLOB não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-130">The BLOB Owner section was not found.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="e0b9d-131"><dt>**\_categoria de blob NMERR \_ \_ não \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-131"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="e0b9d-132">A seção de categoria de BLOB não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-132">The BLOB Category section was not found.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="e0b9d-133"><dt>**NMERR \_ \_ categoria desconhecida**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-133"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="e0b9d-134">A seção de categoria de BLOB foi encontrada, mas não compreendida.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-134">The BLOB Category section was found, but not understood.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="e0b9d-135"><dt>**\_marca desconhecida \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-135"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="e0b9d-136">A seção de marca de BLOB foi encontrada, mas não compreendida.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-136">The BLOB Tag section was found, but not understood.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="e0b9d-137"><dt>**\_erro de \_ conversão de blob NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-137"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="e0b9d-138">O BLOB está corrompido.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-138">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="e0b9d-139"><dt>**NMERR \_ \_ gatilho ilegal**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-139"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="e0b9d-140">A parte do gatilho do BLOB está corrompida.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-140">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="e0b9d-141"><dt>**\_cadeia de blob NMERR \_ \_ inválida**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-141"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="e0b9d-142">A cadeia de caracteres não é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-142">The string is not null-terminated.</span></span><br/>                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="e0b9d-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0b9d-143">Remarks</span></span>

<span data-ttu-id="e0b9d-144">Você deve aplicar esse método para reiniciar um NPP que tenha sido iniciado, interrompido, mas não desconectado.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-144">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="e0b9d-145">O BLOB de erro retornado por *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de configuração especificado em *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="e0b9d-146">O BLOB de erro retornado contém dados de erro que o aplicativo pode usar para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-146">The returned error BLOB contains error data that the application can use for troubleshooting.</span></span> <span data-ttu-id="e0b9d-147">Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar será incluída no blob de erros retornado.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor cannot find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b9d-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0b9d-148">Requirements</span></span>



| <span data-ttu-id="e0b9d-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b9d-149">Requirement</span></span> | <span data-ttu-id="e0b9d-150">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b9d-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b9d-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0b9d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b9d-152">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0b9d-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e0b9d-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0b9d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b9d-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0b9d-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e0b9d-155">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e0b9d-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0b9d-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e0b9d-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b9d-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b9d-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b9d-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0b9d-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0b9d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b9d-160">IRTC</span><span class="sxs-lookup"><span data-stu-id="e0b9d-160">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="e0b9d-161">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="e0b9d-161">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="e0b9d-162">BLOBs de Monitor de Rede</span><span class="sxs-lookup"><span data-stu-id="e0b9d-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




