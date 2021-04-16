---
description: A função createentregatable cria uma tabela de entrega que inclui as informações de conjunto de entrega armazenadas no arquivo INI do analisador.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Função createentregatable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750791"
---
# <a name="createhandofftable-function"></a><span data-ttu-id="99315-103">Função createentregatable</span><span class="sxs-lookup"><span data-stu-id="99315-103">CreateHandoffTable function</span></span>

<span data-ttu-id="99315-104">A função **Createentregatable** cria uma [*tabela de entrega*](h.md) que inclui as informações de conjunto de entrega armazenadas no arquivo ini do analisador.</span><span class="sxs-lookup"><span data-stu-id="99315-104">The **CreateHandoffTable** function creates a [*handoff table*](h.md) that includes the handoff set information stored in the INI file of the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="99315-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99315-105">Syntax</span></span>


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a><span data-ttu-id="99315-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99315-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99315-107">*secName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99315-107">*secName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99315-108">Cadeia de caracteres que indica a seção do arquivo INI onde estão localizadas as informações do conjunto de entrega.</span><span class="sxs-lookup"><span data-stu-id="99315-108">String that indicates the section of the INI file where the handoff set information is located.</span></span>

</dd> <dt>

<span data-ttu-id="99315-109">*iniFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99315-109">*iniFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99315-110">Cadeia de caracteres que inclui o nome do arquivo INI do analisador.</span><span class="sxs-lookup"><span data-stu-id="99315-110">String that includes the name of the parser INI file.</span></span>

</dd> <dt>

<span data-ttu-id="99315-111">*hTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="99315-111">*hTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99315-112">Identificador para uma estrutura de **entrega** criada e mantida pelo monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="99315-112">Handle to a **HANDOFFTABLE** structure created and maintained by Network Monitor.</span></span>

</dd> <dt>

<span data-ttu-id="99315-113">*nMaxProtocolEntries* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99315-113">*nMaxProtocolEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99315-114">Número que especifica o número máximo de entradas que a tabela de entrega pode processar.</span><span class="sxs-lookup"><span data-stu-id="99315-114">Number that specifies the maximum number of entries that the handoff table can process.</span></span>

</dd> <dt>

<span data-ttu-id="99315-115">*base* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99315-115">*base* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99315-116">A base numérica dos números de conjunto de entrega armazenados no arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="99315-116">Numerical base of handoff set numbers stored in the INI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99315-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99315-117">Return value</span></span>

<span data-ttu-id="99315-118">Se a função for bem-sucedida, o valor de retorno será o número de entradas na tabela entrega.</span><span class="sxs-lookup"><span data-stu-id="99315-118">If the function is successful, the return value is the number of entries in the handoff table.</span></span>

<span data-ttu-id="99315-119">Se a função não for bem-sucedida, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="99315-119">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="99315-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="99315-120">Remarks</span></span>

<span data-ttu-id="99315-121">A tabela de entrega criada pelo Monitor de Rede é baseada nas informações fornecidas no analisador INI.</span><span class="sxs-lookup"><span data-stu-id="99315-121">The handoff table created by Network Monitor is based on information provided in the parser INI.</span></span> <span data-ttu-id="99315-122">O identificador retornado para a tabela entrega pode ser usado para obter um identificador para um dos protocolos incluídos na tabela.</span><span class="sxs-lookup"><span data-stu-id="99315-122">The returned handle to the handoff table can then be used to obtain a handle to one of the protocols included in the table.</span></span> <span data-ttu-id="99315-123">Para obter um identificador de um desses protocolos, chame [GetProtocolFromTable](getprotocolfromtable.md).</span><span class="sxs-lookup"><span data-stu-id="99315-123">To obtain a handle of one of these protocols, call [GetProtocolFromTable](getprotocolfromtable.md).</span></span>

<span data-ttu-id="99315-124">Observe que o aplicativo Analisador nunca acessa a estrutura de **entrega** diretamente.</span><span class="sxs-lookup"><span data-stu-id="99315-124">Notice that the parser application never accesses the **HANDOFFTABLE** structure directly.</span></span> <span data-ttu-id="99315-125">Essa estrutura é criada e mantida por Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="99315-125">This structure is created and maintained by Network Monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="99315-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99315-126">Requirements</span></span>



| <span data-ttu-id="99315-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="99315-127">Requirement</span></span> | <span data-ttu-id="99315-128">Valor</span><span class="sxs-lookup"><span data-stu-id="99315-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="99315-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99315-129">Minimum supported client</span></span><br/> | <span data-ttu-id="99315-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99315-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="99315-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99315-131">Minimum supported server</span></span><br/> | <span data-ttu-id="99315-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99315-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="99315-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99315-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="99315-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="99315-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="99315-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99315-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="99315-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99315-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="99315-137">DLL</span><span class="sxs-lookup"><span data-stu-id="99315-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99315-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99315-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99315-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="99315-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99315-140">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="99315-140">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> <dt>

[<span data-ttu-id="99315-141">ENTREGA</span><span class="sxs-lookup"><span data-stu-id="99315-141">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




