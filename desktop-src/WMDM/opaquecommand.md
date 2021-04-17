---
title: Estrutura OPAQUECOMMAND
description: A estrutura OPAQUECOMMAND contém dados para comandos que são passados pelo Windows Media Gerenciador de Dispositivos para um dispositivo, mas que não devem ser afetados pelo Windows Media Gerenciador de Dispositivos.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Estrutura OPAQUECOMMAND Windows Media Gerenciador de Dispositivos
- estruturar Gerenciador de Dispositivos de mídia do Windows
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813204"
---
# <a name="opaquecommand-structure"></a><span data-ttu-id="435b2-105">Estrutura OPAQUECOMMAND</span><span class="sxs-lookup"><span data-stu-id="435b2-105">OPAQUECOMMAND structure</span></span>

<span data-ttu-id="435b2-106">A estrutura **OPAQUECOMMAND** contém dados para comandos que são passados pelo windows media Gerenciador de dispositivos para um dispositivo, mas que não devem ser afetados pelo windows media Gerenciador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="435b2-106">The **OPAQUECOMMAND** structure contains data for commands that are passed through Windows Media Device Manager to a device but are not intended to be acted upon by Windows Media Device Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="435b2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="435b2-107">Syntax</span></span>


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a><span data-ttu-id="435b2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="435b2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="435b2-109">**guidCommand**</span><span class="sxs-lookup"><span data-stu-id="435b2-109">**guidCommand**</span></span>
</dt> <dd>

<span data-ttu-id="435b2-110">**GUID** que representa o comando solicitado.</span><span class="sxs-lookup"><span data-stu-id="435b2-110">**GUID** representing the requested command.</span></span>

</dd> <dt>

<span data-ttu-id="435b2-111">**dwDataLen**</span><span class="sxs-lookup"><span data-stu-id="435b2-111">**dwDataLen**</span></span>
</dt> <dd>

<span data-ttu-id="435b2-112">Comprimento dos dados aos quais *pData* pontos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="435b2-112">Length of the data to which *pData* points, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="435b2-113">**pData**</span><span class="sxs-lookup"><span data-stu-id="435b2-113">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="435b2-114">Dados necessários para executar o comando e/ou dados retornados pelo comando.</span><span class="sxs-lookup"><span data-stu-id="435b2-114">Data required to execute the command, and/or data returned by the command.</span></span>

</dd> <dt>

<span data-ttu-id="435b2-115">**abMAC \[ 20\]**</span><span class="sxs-lookup"><span data-stu-id="435b2-115">**abMAC\[20\]**</span></span>
</dt> <dd>

<span data-ttu-id="435b2-116">Esse código de autenticação de mensagem (MAC) deve incluir o membro **guidCommand** , os dados aos quais *pdwDataLen* aponta e os dados aos quais *pData* aponta, se houver.</span><span class="sxs-lookup"><span data-stu-id="435b2-116">This message authentication code (MAC) should include the **guidCommand** member, the data to which *pdwDataLen* points, and the data to which *pData* points, if any.</span></span> <span data-ttu-id="435b2-117">Se *pData* for **nulo**, ele não deverá ser incluído no Mac.</span><span class="sxs-lookup"><span data-stu-id="435b2-117">If *pData* is **NULL**, it must not be included in the MAC.</span></span> <span data-ttu-id="435b2-118">\_ \_ O comprimento de Mac do WMDM é definido como 20.</span><span class="sxs-lookup"><span data-stu-id="435b2-118">WMDM\_MAC\_LENGTH is defined as 20.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="435b2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="435b2-119">Requirements</span></span>



| <span data-ttu-id="435b2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="435b2-120">Requirement</span></span> | <span data-ttu-id="435b2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="435b2-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="435b2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="435b2-122">Header</span></span><br/> | <dl> <span data-ttu-id="435b2-123"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="435b2-123"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="435b2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="435b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435b2-125">**IMDSPDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="435b2-125">**IMDSPDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="435b2-126">**IMDSPStorage::SendOpaqueCommands**</span><span class="sxs-lookup"><span data-stu-id="435b2-126">**IMDSPStorage::SendOpaqueCommands**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="435b2-127">**IWMDMDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="435b2-127">**IWMDMDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="435b2-128">**IWMDMStorage::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="435b2-128">**IWMDMStorage::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="435b2-129">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="435b2-129">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





