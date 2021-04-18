---
title: Método GetObjectDataOnClearChannel
description: O método GetObjectDataOnClearChannel transfere um bloco de dados de objeto em um canal claro de volta para o Windows Media Gerenciador de Dispositivos.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Método GetObjectDataOnClearChannel Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770535"
---
# <a name="getobjectdataonclearchannel-method"></a><span data-ttu-id="54d37-104">Método GetObjectDataOnClearChannel</span><span class="sxs-lookup"><span data-stu-id="54d37-104">GetObjectDataOnClearChannel method</span></span>

<span data-ttu-id="54d37-105">O método **GetObjectDataOnClearChannel** transfere um bloco de dados de objeto em um canal claro de volta para o Windows Media Gerenciador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="54d37-105">The **GetObjectDataOnClearChannel** method transfers a block of object data on a clear channel back to Windows Media Device Manager.</span></span>

<span data-ttu-id="54d37-106">Esse método é idêntico a [**ISCPSecureExchange:: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , exceto que os dados retornados por esse método não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="54d37-106">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="54d37-107">Consequentemente, esse método é mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="54d37-107">Consequently this method is more efficient.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d37-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54d37-108">Syntax</span></span>


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="54d37-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54d37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d37-110">*pDevice*</span><span class="sxs-lookup"><span data-stu-id="54d37-110">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="54d37-111">Ponteiro para o objeto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54d37-111">Pointer to the device object.</span></span>

</dd> <dt>

<span data-ttu-id="54d37-112">*pData*</span><span class="sxs-lookup"><span data-stu-id="54d37-112">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="54d37-113">Ponteiro para um buffer para receber dados.</span><span class="sxs-lookup"><span data-stu-id="54d37-113">Pointer to a buffer to receive data.</span></span>

</dd> <dt>

<span data-ttu-id="54d37-114">*pdwSize*</span><span class="sxs-lookup"><span data-stu-id="54d37-114">*pdwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="54d37-115">Ponteiro para um **DWORD** que contém o tamanho da transferência.</span><span class="sxs-lookup"><span data-stu-id="54d37-115">Pointer to a **DWORD** containing the transfer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d37-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54d37-116">Return value</span></span>

<span data-ttu-id="54d37-117">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54d37-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="54d37-118">Se o método falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="54d37-118">If the method fails, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="54d37-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="54d37-119">Return code</span></span>                                                                                                | <span data-ttu-id="54d37-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="54d37-120">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="54d37-121"><dt>**\_ \_ \_ falha na verificação de Mac E WMDM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="54d37-121"><dt>**WMDM\_E\_MAC\_CHECK\_FAILED**</dt></span></span> </dl> | <span data-ttu-id="54d37-122">O código de autenticação da mensagem não é válido.</span><span class="sxs-lookup"><span data-stu-id="54d37-122">The message authentication code is not valid.</span></span><br/>                                    |
| <dl> <span data-ttu-id="54d37-123"><dt>**WMDM \_ E não \_ à direita**</dt></span><span class="sxs-lookup"><span data-stu-id="54d37-123"><dt>**WMDM\_E\_NORIGHTS**</dt></span></span> </dl>           | <span data-ttu-id="54d37-124">O chamador não tem os direitos necessários para executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="54d37-124">The caller does not have the rights required to perform the requested operation.</span></span><br/> |
| <dl> <span data-ttu-id="54d37-125"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="54d37-125"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="54d37-126">O método falhou.</span><span class="sxs-lookup"><span data-stu-id="54d37-126">The method failed.</span></span> <span data-ttu-id="54d37-127">Terminar a interação com o provedor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="54d37-127">Terminate interaction with the content provider.</span></span><br/>              |
| <dl> <span data-ttu-id="54d37-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="54d37-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="54d37-129">Um parâmetro é um ponteiro inválido ou **nulo** .</span><span class="sxs-lookup"><span data-stu-id="54d37-129">A parameter is an invalid or **NULL** pointer.</span></span><br/>                                   |
| <dl> <span data-ttu-id="54d37-130"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="54d37-130"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="54d37-131">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="54d37-131">An unspecified error occurred.</span></span><br/>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="54d37-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="54d37-132">Remarks</span></span>

<span data-ttu-id="54d37-133">Para transferir dados, o Windows Media Gerenciador de Dispositivos chama o método [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) para obter os dados do contêiner.</span><span class="sxs-lookup"><span data-stu-id="54d37-133">To transfer data, Windows Media Device Manager calls the [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) method to obtain the container data.</span></span> <span data-ttu-id="54d37-134">Em seguida, **GetObjectDataOnClearChannel** é chamado para transferir blocos de dados de objeto do provedor de conteúdo para o Windows Media Gerenciador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="54d37-134">**GetObjectDataOnClearChannel** is then called to transfer blocks of object data from the content provider to Windows Media Device Manager.</span></span> <span data-ttu-id="54d37-135">Se S \_ OK for retornado com *pdwSize* definido como zero, o Windows Media Gerenciador de dispositivos não solicitará mais dados.</span><span class="sxs-lookup"><span data-stu-id="54d37-135">If S\_OK is returned with *pdwSize* set to zero, Windows Media Device Manager will request no further data.</span></span>

<span data-ttu-id="54d37-136">Esse método é idêntico a [**ISCPSecureExchange:: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , exceto que os dados retornados por esse método não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="54d37-136">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="54d37-137">Consequentemente, esse método é mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="54d37-137">Consequently this method is more efficient.</span></span>

## <a name="requirements"></a><span data-ttu-id="54d37-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54d37-138">Requirements</span></span>



| <span data-ttu-id="54d37-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="54d37-139">Requirement</span></span> | <span data-ttu-id="54d37-140">Valor</span><span class="sxs-lookup"><span data-stu-id="54d37-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54d37-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54d37-141">Header</span></span><br/>  | <dl> <span data-ttu-id="54d37-142"><dt>WMSCP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54d37-142"><dt>WMSCP.idl</dt></span></span> </dl>    |
| <span data-ttu-id="54d37-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54d37-143">Library</span></span><br/> | <dl> <span data-ttu-id="54d37-144"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54d37-144"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54d37-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="54d37-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d37-146">**ISCPSecureExchange:: objectdata**</span><span class="sxs-lookup"><span data-stu-id="54d37-146">**ISCPSecureExchange::ObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[<span data-ttu-id="54d37-147">**Interface ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="54d37-147">**ISCPSecureExchange3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





