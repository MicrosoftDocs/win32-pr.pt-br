---
description: Seleciona uma NIC de registro.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Função GetNPPBlobFromUI (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922004"
---
# <a name="getnppblobfromui-function"></a><span data-ttu-id="f30c3-103">Função GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="f30c3-103">GetNPPBlobFromUI function</span></span>

<span data-ttu-id="f30c3-104">A função **GetNPPBlobFromUI** seleciona uma NIC de registro.</span><span class="sxs-lookup"><span data-stu-id="f30c3-104">The **GetNPPBlobFromUI** function selects a register NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="f30c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f30c3-105">Syntax</span></span>


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="f30c3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f30c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f30c3-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f30c3-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f30c3-108">Um identificador para uma janela que exibe a caixa de diálogo **selecionar uma rede** .</span><span class="sxs-lookup"><span data-stu-id="f30c3-108">A handle to a window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="f30c3-109">*hFilterBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f30c3-109">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f30c3-110">Um identificador para um [*blob de filtro*](f.md) usado para limitar quais NICs são exibidos.</span><span class="sxs-lookup"><span data-stu-id="f30c3-110">A handle to a [*filter BLOB*](f.md) used to limit which NICs are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="f30c3-111">*phBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f30c3-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f30c3-112">Um ponteiro para o identificador do BLOB que representa a NIC selecionada.</span><span class="sxs-lookup"><span data-stu-id="f30c3-112">A pointer to the handle of the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f30c3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f30c3-113">Return value</span></span>

<span data-ttu-id="f30c3-114">Se a função for bem-sucedida (o usuário seleciona uma NIC), o valor de retorno será NMERR com \_ êxito e o blob ao qual *phBlob* aponta será preenchido.</span><span class="sxs-lookup"><span data-stu-id="f30c3-114">If the function is successful (the user selects a NIC), the return value is NMERR\_SUCCESS, and the BLOB that *phBlob* points to is filled in.</span></span>

<span data-ttu-id="f30c3-115">Se o usuário não selecionar uma NIC, o valor de retorno será **NMERR \_ nenhum \_ NPP \_ selecionado**.</span><span class="sxs-lookup"><span data-stu-id="f30c3-115">If the user does not select an NIC, the return value is **NMERR\_NO\_NPP\_SELECTED**.</span></span>

<span data-ttu-id="f30c3-116">Se a função não for bem-sucedida, o valor de retorno será outro valor de NMERR.</span><span class="sxs-lookup"><span data-stu-id="f30c3-116">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f30c3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f30c3-117">Remarks</span></span>

<span data-ttu-id="f30c3-118">Quando chamado, Monitor de Rede exibe a caixa de diálogo **selecionar uma rede** , que pode ser usada para selecionar uma NIC.</span><span class="sxs-lookup"><span data-stu-id="f30c3-118">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="f30c3-119">O BLOB NPP que representa a NIC é retornado para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="f30c3-119">The NPP BLOB that represents the NIC is returned to the calling application.</span></span>

<span data-ttu-id="f30c3-120">Se o BLOB nomeado por *hFilterBlob* for um [*blob especial*](s.md), o localizador tentará processá-lo.</span><span class="sxs-lookup"><span data-stu-id="f30c3-120">If the BLOB named by *hFilterBlob* is a [*special BLOB*](s.md), the finder will attempt to process it.</span></span> <span data-ttu-id="f30c3-121">Um exemplo seria uma chamada que anteriormente retornava um BLOB especial do NPP remoto.</span><span class="sxs-lookup"><span data-stu-id="f30c3-121">An example would be a call that had previously returned a special BLOB from the remote NPP.</span></span> <span data-ttu-id="f30c3-122">O aplicativo inseriu a marca necessária, \_ nome do computador.</span><span class="sxs-lookup"><span data-stu-id="f30c3-122">The application inserted the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="f30c3-123">Nessa situação, o localizador passaria esse BLOB para o NPP remoto, que retornaria uma tabela de BLOBs NPP que representa o computador solicitado.</span><span class="sxs-lookup"><span data-stu-id="f30c3-123">In this situation, the finder would pass this BLOB to the remote NPP, which would then return a table of NPP BLOBs representing the machine requested.</span></span> <span data-ttu-id="f30c3-124">Esses BLOBs de NPP remotos seriam exibidos na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f30c3-124">These remote NPP BLOBs would appear in the dialog box.</span></span>

<span data-ttu-id="f30c3-125">O chamador deve chamar a função [DestroyBlob](destroyblob.md) , que destrói o blob retornado quando ele não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="f30c3-125">The caller must call the [DestroyBlob](destroyblob.md) function, which destroys the returned BLOB when it is no longer required.</span></span>



| <span data-ttu-id="f30c3-126">Para saber mais sobre</span><span class="sxs-lookup"><span data-stu-id="f30c3-126">For more information about</span></span> | <span data-ttu-id="f30c3-127">Consulte</span><span class="sxs-lookup"><span data-stu-id="f30c3-127">See</span></span>                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f30c3-128">Três maneiras de selecionar NICs</span><span class="sxs-lookup"><span data-stu-id="f30c3-128">Three ways to select NICs</span></span>  | [<span data-ttu-id="f30c3-129">Selecionando uma placa de interface de rede</span><span class="sxs-lookup"><span data-stu-id="f30c3-129">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |
| <span data-ttu-id="f30c3-130">Especificando um BLOB de filtro</span><span class="sxs-lookup"><span data-stu-id="f30c3-130">Specifying a filter BLOB</span></span>   | [<span data-ttu-id="f30c3-131">Especificando um BLOB de filtro</span><span class="sxs-lookup"><span data-stu-id="f30c3-131">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a><span data-ttu-id="f30c3-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f30c3-132">Requirements</span></span>



| <span data-ttu-id="f30c3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f30c3-133">Requirement</span></span> | <span data-ttu-id="f30c3-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f30c3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f30c3-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f30c3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f30c3-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f30c3-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f30c3-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f30c3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f30c3-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f30c3-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f30c3-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f30c3-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f30c3-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f30c3-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="f30c3-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f30c3-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="f30c3-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f30c3-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="f30c3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f30c3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f30c3-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f30c3-144"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f30c3-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="f30c3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f30c3-146">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="f30c3-146">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="f30c3-147">SelectNPPBlobFromTable</span><span class="sxs-lookup"><span data-stu-id="f30c3-147">SelectNPPBlobFromTable</span></span>](selectnppblobfromtable.md)
</dt> </dl>

 

 




