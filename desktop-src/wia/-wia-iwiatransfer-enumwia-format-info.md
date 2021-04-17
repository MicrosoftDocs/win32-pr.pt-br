---
description: Cria um enumerador para os formatos de transferência aos quais o dispositivo de aquisição de imagem do Windows (WIA) 2,0 dá suporte.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'Método IWiaTransfer:: EnumWIA_FORMAT_INFO (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770475"
---
# <a name="iwiatransferenumwia_format_info-method"></a><span data-ttu-id="b51d9-103">Método de informações de \_ formato IWiaTransfer:: EnumWIA \_</span><span class="sxs-lookup"><span data-stu-id="b51d9-103">IWiaTransfer::EnumWIA\_FORMAT\_INFO method</span></span>

<span data-ttu-id="b51d9-104">Cria um enumerador para os formatos de transferência aos quais o dispositivo de aquisição de imagem do Windows (WIA) 2,0 dá suporte.</span><span class="sxs-lookup"><span data-stu-id="b51d9-104">Creates an enumerator for the transfer formats that the Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="b51d9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b51d9-105">Syntax</span></span>


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="b51d9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b51d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b51d9-107">*ppIEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b51d9-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b51d9-108">Tipo: **[ **\_ \_ informações de formato IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="b51d9-108">Type: **[**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span></span>

<span data-ttu-id="b51d9-109">O endereço do ponteiro para a interface [**de \_ \_ informações de formato IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) para o enumerador.</span><span class="sxs-lookup"><span data-stu-id="b51d9-109">The address of the pointer to the [**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) interface for the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b51d9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b51d9-110">Return value</span></span>

<span data-ttu-id="b51d9-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b51d9-111">Type: **HRESULT**</span></span>

<span data-ttu-id="b51d9-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b51d9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b51d9-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b51d9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b51d9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b51d9-114">Remarks</span></span>

<span data-ttu-id="b51d9-115">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro de interface recebido por meio do parâmetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="b51d9-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointer received through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b51d9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b51d9-116">Requirements</span></span>



| <span data-ttu-id="b51d9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b51d9-117">Requirement</span></span> | <span data-ttu-id="b51d9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b51d9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b51d9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b51d9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b51d9-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b51d9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b51d9-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b51d9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b51d9-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b51d9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b51d9-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b51d9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b51d9-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b51d9-124"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="b51d9-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="b51d9-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b51d9-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b51d9-126"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="b51d9-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b51d9-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b51d9-128"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b51d9-128"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
