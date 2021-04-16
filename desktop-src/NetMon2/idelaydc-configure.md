---
description: O método configure envia informações de configuração usadas para uma captura.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Método IDelaydCConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460958"
---
# <a name="idelaydcconfigure-method"></a><span data-ttu-id="5c7e2-103">Método IDelaydC:: Configure</span><span class="sxs-lookup"><span data-stu-id="5c7e2-103">IDelaydC::Configure method</span></span>

<span data-ttu-id="5c7e2-104">O método **Configure** envia informações de configuração usadas para uma captura.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-104">The **Configure** method submits configuration information used for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c7e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c7e2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="5c7e2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c7e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c7e2-107">*hConfigurationBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c7e2-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c7e2-108">Identificador para o BLOB que contém as informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-108">Handle to the BLOB that contains the configuration information.</span></span>

</dd> <dt>

<span data-ttu-id="5c7e2-109">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c7e2-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c7e2-110">Identificador para um BLOB de erro que contém informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="5c7e2-111">Para obter informações sobre o conteúdo de um BLOB de erro, consulte a seção comentários neste tópico.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-111">For information about the contents of an error BLOB, see the Remarks section in this topic .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c7e2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c7e2-112">Return value</span></span>

<span data-ttu-id="5c7e2-113">Se esse método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-113">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5c7e2-114">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="5c7e2-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5c7e2-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5c7e2-115">Return code</span></span>                                                                                                      | <span data-ttu-id="5c7e2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c7e2-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c7e2-117"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7e2-117"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                  | <span data-ttu-id="5c7e2-118">O NPP relata que a sessão de captura foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-118">The NPP reports that the capture session has started.</span></span><br/>                          |
| <dl> <span data-ttu-id="5c7e2-119"><dt>**\_disco NMERR \_ não \_ local \_ fixo**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7e2-119"><dt>**NMERR\_DISK\_NOT\_LOCAL\_FIXED**</dt></span></span> </dl>    |                                                                                           |
| <dl> <span data-ttu-id="5c7e2-120"><dt>**NMERR \_ \_ não pôde \_ criar \_ memória**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7e2-120"><dt>**NMERR\_COULD\_NOT\_CREATE\_MEMORY**</dt></span></span> </dl> |                                                                                           |
| <dl> <span data-ttu-id="5c7e2-121"><dt>**NMERR \_ \_ de \_ memória insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7e2-121"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>            | <span data-ttu-id="5c7e2-122">Não havia memória disponível.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-122">No memory was available.</span></span> <span data-ttu-id="5c7e2-123">Desligue o Windows para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-123">Shut down windows to free up resources.</span></span><br/>               |
| <dl> <span data-ttu-id="5c7e2-124"><dt>**NMERR \_ \_ parâmetro inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7e2-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="5c7e2-125">O BLOB de configuração especificado pelo parâmetro hConfiguration não é válido.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-125">The configuration BLOB specified by the hConfiguration parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c7e2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c7e2-126">Remarks</span></span>

<span data-ttu-id="5c7e2-127">Você deve aplicar esse método para reiniciar um NPP que tenha sido iniciado, interrompido, mas não desconectado.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-127">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="5c7e2-128">O BLOB de erro retornado por *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de configuração especificado em *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-128">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="5c7e2-129">O BLOB de erro retornado contém informações de erro que o aplicativo pode usar para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-129">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="5c7e2-130">Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar é incluída no blob de erros retornado.</span><span class="sxs-lookup"><span data-stu-id="5c7e2-130">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c7e2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c7e2-131">Requirements</span></span>



| <span data-ttu-id="5c7e2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c7e2-132">Requirement</span></span> | <span data-ttu-id="5c7e2-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5c7e2-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7e2-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c7e2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7e2-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c7e2-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5c7e2-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c7e2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7e2-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c7e2-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5c7e2-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5c7e2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c7e2-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c7e2-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5c7e2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5c7e2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c7e2-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c7e2-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c7e2-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c7e2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c7e2-143">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="5c7e2-143">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="5c7e2-144">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="5c7e2-144">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="5c7e2-145">IDelaydC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="5c7e2-145">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="5c7e2-146">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="5c7e2-146">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




