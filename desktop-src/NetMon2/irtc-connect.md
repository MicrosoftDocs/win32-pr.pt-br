---
description: 'Método IRTC:: Connect – o método Connect conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração para a conexão.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'Método IRTC:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110737"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="4f8f7-103">Método IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="4f8f7-103">IRTC::Connect method</span></span>

<span data-ttu-id="4f8f7-104">O método **Connect** conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração para a conexão.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f8f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f8f7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="4f8f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f8f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f8f7-107">*hInputBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f8f7-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8f7-108">Identificador para o BLOB que especifica a NIC à qual você está se conectando e as informações de configuração para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="4f8f7-109">*StatusCallbackProc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f8f7-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8f7-110">Endereço da função de retorno de chamada de status do usuário, que recebe atualizações de status, como gatilhos.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="4f8f7-111">Esse parâmetro pode ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4f8f7-112">*FramesCallbackProc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f8f7-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8f7-113">Endereço da função de retorno de chamada de quadro do usuário, que é usada para receber atualizações de status, como gatilhos.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="4f8f7-114">Esse parâmetro pode ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4f8f7-115">*UserContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f8f7-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8f7-116">Valor passado quando a função de retorno de chamada de status e quadro do usuário é chamada.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="4f8f7-117">Se ambas as funções de retorno de chamada forem especificadas, elas deverão usar o mesmo valor de contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="4f8f7-118">O valor desse parâmetro é normalmente o HWND ou um ponteiro ' this '.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="4f8f7-119">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4f8f7-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8f7-120">Identificador para um BLOB de erro que contém informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="4f8f7-121">Consulte os comentários na parte inferior deste tópico para obter informações sobre o que está no BLOB de erros.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f8f7-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4f8f7-122">Return value</span></span>

<span data-ttu-id="4f8f7-123">Se esse método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4f8f7-124">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro (que incluem os erros retornados pela chamada interna **IRTC:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="4f8f7-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="4f8f7-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4f8f7-125">Return code</span></span>                                                                                                         | <span data-ttu-id="4f8f7-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f8f7-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f8f7-127"><dt>**NMERR \_ já \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="4f8f7-128">Esta instância do objeto COM NPP já está conectada à rede.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="4f8f7-129"><dt>**\_erro de \_ conversão de blob NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="4f8f7-130">O BLOB de configuração está corrompido.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="4f8f7-131">Esse erro é gerado pela chamada **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="4f8f7-132"><dt>**a \_ entrada de blob NMERR não \_ \_ \_ \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="4f8f7-133">O BLOB de entrada especificado pelo parâmetro *hInputBlob* não tem uma entrada necessária para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="4f8f7-134">Esse erro pode ser gerado pela chamada **IRTC:: Connect** ou **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="4f8f7-135">Examine o BLOB de erro retornado por *hErrorBlob* para determinar qual entrada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="4f8f7-136"><dt>**\_blob NMERR \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="4f8f7-137">A função **createBlob** não foi chamada.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="4f8f7-138">Esse erro é gerado pela chamada **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="4f8f7-139"><dt>**\_cadeia de blob NMERR \_ \_ inválida**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="4f8f7-140">A cadeia de caracteres não é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-140">The string is not null-terminated.</span></span> <span data-ttu-id="4f8f7-141">Esse erro é gerado pela chamada **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="4f8f7-142"><dt>**NMERR \_ \_ gatilho ilegal**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="4f8f7-143">A parte do gatilho do BLOB de entrada está corrompida.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="4f8f7-144">Esse erro é gerado pela chamada **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="4f8f7-145"><dt>**NMERR \_ \_ blob inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="4f8f7-146">O objeto especificado em *hInputBlob* não é um blob.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="4f8f7-147">Esse erro é gerado pela chamada **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="4f8f7-148"><dt>**NMERR \_ \_ de \_ memória insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="4f8f7-149">A memória necessária para executar essa operação não está disponível.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="4f8f7-150">Esse erro é gerado pela chamada **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="4f8f7-151"><dt>**\_tempo limite de NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="4f8f7-152">O tempo limite da solicitação foi atingido. Esse erro é gerado pela chamada **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="4f8f7-153"><dt>**BLOB de upNMERR de \_ nível \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="4f8f7-154">O número de versão do BLOB especificado em *hInputBlob* está incorreto.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="4f8f7-155">Esse erro é gerado pela chamada **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="4f8f7-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f8f7-156">Remarks</span></span>

<span data-ttu-id="4f8f7-157">Quando o método **Connect** é chamado, o NPP chama automaticamente o método **IRTC:: Configure** usando o blob fornecido pelo *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="4f8f7-158">Observe que todos os códigos de erro retornados pela chamada para **IRTC:: Configure** são passados de volta e retornados pela chamada **IRTC:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="4f8f7-159">Esse método deve ser chamado antes que você possa iniciar a captura de quadros.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="4f8f7-160">Observe que quando você se conecta à rede usando esse método, você deve continuar a usar a interface **IRTC** para capturar quadros.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="4f8f7-161">Ao chamar essa função, você deve especificar uma função de retorno de chamada de status ou quadro, mesmo que atue apenas como um espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="4f8f7-162">O BLOB de entrada especificado por *hInputBlob* pode ser obtido chamando os métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable** .</span><span class="sxs-lookup"><span data-stu-id="4f8f7-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="4f8f7-163">O BLOB de erro retornado em *hErrorBlob* contém informações de erro que o desenvolvedor ou o aplicativo pode usar para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="4f8f7-164">O BLOB de erro retornado por *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de entrada especificado em *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="4f8f7-165">Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar é incluída no blob de erros retornado.</span><span class="sxs-lookup"><span data-stu-id="4f8f7-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="4f8f7-166">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="4f8f7-166">For information about</span></span>                          | <span data-ttu-id="4f8f7-167">Consulte</span><span class="sxs-lookup"><span data-stu-id="4f8f7-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4f8f7-168">Obtendo o BLOB de entrada que representa uma NIC</span><span class="sxs-lookup"><span data-stu-id="4f8f7-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="4f8f7-169">Selecionando uma placa de interface de rede</span><span class="sxs-lookup"><span data-stu-id="4f8f7-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="4f8f7-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f8f7-170">Requirements</span></span>



| <span data-ttu-id="4f8f7-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f8f7-171">Requirement</span></span> | <span data-ttu-id="4f8f7-172">Valor</span><span class="sxs-lookup"><span data-stu-id="4f8f7-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8f7-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f8f7-173">Minimum supported client</span></span><br/> | <span data-ttu-id="4f8f7-174">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4f8f7-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4f8f7-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f8f7-175">Minimum supported server</span></span><br/> | <span data-ttu-id="4f8f7-176">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4f8f7-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4f8f7-177">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4f8f7-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f8f7-178"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4f8f7-179">DLL</span><span class="sxs-lookup"><span data-stu-id="4f8f7-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f8f7-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f8f7-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f8f7-181">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4f8f7-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f8f7-182">IRTC</span><span class="sxs-lookup"><span data-stu-id="4f8f7-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="4f8f7-183">IRTC:: configurar</span><span class="sxs-lookup"><span data-stu-id="4f8f7-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="4f8f7-184">IRTC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="4f8f7-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="4f8f7-185">IRTC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="4f8f7-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




