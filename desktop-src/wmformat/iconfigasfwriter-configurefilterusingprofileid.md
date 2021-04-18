---
title: Método IConfigAsfWriter ConfigureFilterUsingProfileId
description: O método ConfigureFilterUsingProfileId configura o filtro para gravar um arquivo ASF com um índice de identificador de perfil (ID) da lista de perfis do sistema. (Somente para perfis do Windows Media Format 4,0.).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Formato de mídia do Windows do método ConfigureFilterUsingProfileId
- Método ConfigureFilterUsingProfileId Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método ConfigureFilterUsingProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105793827"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a><span data-ttu-id="ca4e7-107">Método IConfigAsfWriter:: ConfigureFilterUsingProfileId</span><span class="sxs-lookup"><span data-stu-id="ca4e7-107">IConfigAsfWriter::ConfigureFilterUsingProfileId method</span></span>

<span data-ttu-id="ca4e7-108">O método **ConfigureFilterUsingProfileId** configura o filtro para gravar um arquivo ASF com um índice de identificador de perfil (ID) da lista de perfis do sistema.</span><span class="sxs-lookup"><span data-stu-id="ca4e7-108">The **ConfigureFilterUsingProfileId** method configures the filter to write an ASF file with a profile identifier (ID) index from the system profile list.</span></span> <span data-ttu-id="ca4e7-109">(Somente para perfis do Windows Media Format 4,0.)</span><span class="sxs-lookup"><span data-stu-id="ca4e7-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="ca4e7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca4e7-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="ca4e7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca4e7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca4e7-112">*dwProfileId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca4e7-112">*dwProfileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca4e7-113">ID do perfil, conforme definido na versão 4,0 do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ca4e7-113">Profile ID as defined in version 4.0 of the Windows Media Format SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca4e7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca4e7-114">Return value</span></span>

<span data-ttu-id="ca4e7-115">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca4e7-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="ca4e7-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ca4e7-116">Return code</span></span>                                                                                         | <span data-ttu-id="ca4e7-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca4e7-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="ca4e7-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca4e7-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="ca4e7-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ca4e7-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="ca4e7-120"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="ca4e7-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="ca4e7-121">O perfil não é válido.</span><span class="sxs-lookup"><span data-stu-id="ca4e7-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="ca4e7-122"><dt>**VFW \_ E \_ estado incorreto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ca4e7-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="ca4e7-123">O grafo de filtro é interrompido.</span><span class="sxs-lookup"><span data-stu-id="ca4e7-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca4e7-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca4e7-124">Remarks</span></span>

<span data-ttu-id="ca4e7-125">Este método agora é obsoleto porque ele pressupõe os perfis do SDK do Windows Media Format versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="ca4e7-125">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="ca4e7-126">Para configurar o filtro para a versão 7,0 e perfis posteriores, use [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) ou [**IConfigAsfWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span><span class="sxs-lookup"><span data-stu-id="ca4e7-126">To configure the filter for version 7.0 and later profiles, use [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) or [**IConfigAsfWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ca4e7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca4e7-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca4e7-128">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca4e7-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

