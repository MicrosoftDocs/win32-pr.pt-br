---
title: Método IWMDRMLicenseManagement CreateLicenseRevocationChallenge (wmdrmsdk. h)
description: O método CreateLicenseRevocationChallenge gera um desafio de revogação de licença.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Formato de mídia do Windows do método CreateLicenseRevocationChallenge
- Método CreateLicenseRevocationChallenge Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método CreateLicenseRevocationChallenge
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815499"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a><span data-ttu-id="aaf82-106">Método IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge</span><span class="sxs-lookup"><span data-stu-id="aaf82-106">IWMDRMLicenseManagement::CreateLicenseRevocationChallenge method</span></span>

<span data-ttu-id="aaf82-107">O método **CreateLicenseRevocationChallenge** gera um desafio de revogação de licença.</span><span class="sxs-lookup"><span data-stu-id="aaf82-107">The **CreateLicenseRevocationChallenge** method generates a license revocation challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf82-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aaf82-108">Syntax</span></span>


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a><span data-ttu-id="aaf82-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aaf82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaf82-110">*pbMachineID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aaf82-110">*pbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf82-111">Identificador de máquina especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="aaf82-111">User-specified machine identifier.</span></span> <span data-ttu-id="aaf82-112">Esse valor é usado para consultar uma licença no servidor e deve estar de acordo com qualquer formato que o servidor de licença usa.</span><span class="sxs-lookup"><span data-stu-id="aaf82-112">This value is used to query for a license on the server and must conform to whatever format the license server uses.</span></span>

</dd> <dt>

<span data-ttu-id="aaf82-113">*cbMachineID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aaf82-113">*cbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf82-114">Tamanho, em bytes, do identificador da máquina.</span><span class="sxs-lookup"><span data-stu-id="aaf82-114">Size, in bytes, of the machine identifier.</span></span>

</dd> <dt>

<span data-ttu-id="aaf82-115">*pbChallenge* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aaf82-115">*pbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf82-116">Dados de desafio especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="aaf82-116">User-specified challenge data.</span></span> <span data-ttu-id="aaf82-117">Esses dados, além do identificador da máquina, são usados para consultar o servidor de licença para que as licenças sejam revogadas.</span><span class="sxs-lookup"><span data-stu-id="aaf82-117">This data, in addition to the machine identifier, is used to query the license server for licenses to be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="aaf82-118">*cbChallenge* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aaf82-118">*cbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf82-119">Tamanho, em bytes, dos dados de desafio.</span><span class="sxs-lookup"><span data-stu-id="aaf82-119">Size, in bytes, of the challenge data.</span></span>

</dd> <dt>

<span data-ttu-id="aaf82-120">*ppbChallengeOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aaf82-120">*ppbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf82-121">Endereço de um ponteiro que recebe o endereço da saída de desafio.</span><span class="sxs-lookup"><span data-stu-id="aaf82-121">Address of a pointer that receives the address of the challenge output.</span></span> <span data-ttu-id="aaf82-122">Esse buffer é o dado que é enviado para o serviço de revogação de licença.</span><span class="sxs-lookup"><span data-stu-id="aaf82-122">This buffer is the data that is sent to the license revocation service.</span></span> <span data-ttu-id="aaf82-123">Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="aaf82-123">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="aaf82-124">*pcbChallengeOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aaf82-124">*pcbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf82-125">Endereço de uma variável que recebe o tamanho dos dados de saída de desafio alocados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="aaf82-125">Address of a variable that receives the size of the allocated challenge output data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaf82-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aaf82-126">Return value</span></span>

<span data-ttu-id="aaf82-127">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="aaf82-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="aaf82-128">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aaf82-128">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="aaf82-129">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="aaf82-129">Return code</span></span>                                                                          | <span data-ttu-id="aaf82-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="aaf82-130">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="aaf82-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf82-131"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="aaf82-132">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="aaf82-132">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aaf82-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="aaf82-133">Remarks</span></span>

<span data-ttu-id="aaf82-134">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="aaf82-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaf82-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaf82-135">Requirements</span></span>



| <span data-ttu-id="aaf82-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaf82-136">Requirement</span></span> | <span data-ttu-id="aaf82-137">Valor</span><span class="sxs-lookup"><span data-stu-id="aaf82-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf82-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aaf82-138">Header</span></span><br/> | <dl> <span data-ttu-id="aaf82-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaf82-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaf82-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="aaf82-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf82-141">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="aaf82-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





