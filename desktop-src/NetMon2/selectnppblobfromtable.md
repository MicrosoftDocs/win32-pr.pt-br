---
description: A função SelectNPPBlobFromTable seleciona uma NIC de uma tabela de BLOB NPP fornecida.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Função SelectNPPBlobFromTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164635"
---
# <a name="selectnppblobfromtable-function"></a><span data-ttu-id="b385b-103">Função SelectNPPBlobFromTable</span><span class="sxs-lookup"><span data-stu-id="b385b-103">SelectNPPBlobFromTable function</span></span>

<span data-ttu-id="b385b-104">A função **SelectNPPBlobFromTable** seleciona uma NIC de uma tabela de blob NPP fornecida.</span><span class="sxs-lookup"><span data-stu-id="b385b-104">The **SelectNPPBlobFromTable** function selects a NIC from a supplied NPP BLOB table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b385b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b385b-105">Syntax</span></span>


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="b385b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b385b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b385b-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b385b-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b385b-108">Identificador para a janela que exibe a caixa de diálogo **selecionar uma rede** .</span><span class="sxs-lookup"><span data-stu-id="b385b-108">Handle to the window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b385b-109">*pBlobTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b385b-109">*pBlobTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b385b-110">Ponteiro para a tabela de BLOB fornecida.</span><span class="sxs-lookup"><span data-stu-id="b385b-110">Pointer to the supplied BLOB table.</span></span> <span data-ttu-id="b385b-111">Monitor de Rede usa essa tabela para preencher a caixa de diálogo **selecionar uma rede** .</span><span class="sxs-lookup"><span data-stu-id="b385b-111">Network Monitor uses this table to populate the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b385b-112">*hBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b385b-112">*hBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b385b-113">Identificador para o BLOB que representa a NIC selecionada.</span><span class="sxs-lookup"><span data-stu-id="b385b-113">Handle to the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b385b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b385b-114">Return value</span></span>

<span data-ttu-id="b385b-115">Se a função for bem-sucedida e o usuário selecionar uma NIC, o valor de retorno será NMERR \_ Success; o blob apontado por *hBlob* será preenchido.</span><span class="sxs-lookup"><span data-stu-id="b385b-115">If the function is successful and the user selects a NIC, the return value is NMERR\_SUCCESS; the BLOB pointed to by *hBlob* is filled in.</span></span>

<span data-ttu-id="b385b-116">Se o usuário não selecionar uma NIC, o valor de retorno será NMERR \_ nenhum \_ NPP \_ selecionado.</span><span class="sxs-lookup"><span data-stu-id="b385b-116">If the user does not select a NIC, the return value is NMERR\_NO\_NPP\_SELECTED.</span></span>

<span data-ttu-id="b385b-117">Se a função não for bem-sucedida, o valor de retorno será outro valor de NMERR.</span><span class="sxs-lookup"><span data-stu-id="b385b-117">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b385b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b385b-118">Remarks</span></span>

<span data-ttu-id="b385b-119">Quando chamado, Monitor de Rede exibe a caixa de diálogo **selecionar uma rede** , que pode ser usada para selecionar uma NIC.</span><span class="sxs-lookup"><span data-stu-id="b385b-119">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="b385b-120">O BLOB NPP que representa a NIC selecionada retorna para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="b385b-120">The NPP BLOB that represents the selected NIC returns to the calling application.</span></span>

<span data-ttu-id="b385b-121">Para aprender as várias maneiras que você pode selecionar NICs, consulte [selecionando uma placa de interface de rede](selecting-a-network-interface-card.md)</span><span class="sxs-lookup"><span data-stu-id="b385b-121">To learn the various ways you can select NICs, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="b385b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b385b-122">Requirements</span></span>



| <span data-ttu-id="b385b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b385b-123">Requirement</span></span> | <span data-ttu-id="b385b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b385b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b385b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b385b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b385b-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b385b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b385b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b385b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b385b-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b385b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b385b-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b385b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b385b-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b385b-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b385b-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b385b-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="b385b-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b385b-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b385b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b385b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b385b-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b385b-134"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b385b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b385b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b385b-136">GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="b385b-136">GetNPPBlobFromUI</span></span>](getnppblobfromui.md)
</dt> <dt>

[<span data-ttu-id="b385b-137">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="b385b-137">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="b385b-138">Entradas de BLOB especiais</span><span class="sxs-lookup"><span data-stu-id="b385b-138">Special BLOB Entries</span></span>](special-blob-entries.md)
</dt> </dl>

 

 




