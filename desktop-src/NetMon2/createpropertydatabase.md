---
description: A função CreatePropertyDatabase cria um banco de dados de propriedade que armazena as propriedades de um protocolo.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Função CreatePropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812892"
---
# <a name="createpropertydatabase-function"></a><span data-ttu-id="afe0e-103">Função CreatePropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="afe0e-103">CreatePropertyDatabase function</span></span>

<span data-ttu-id="afe0e-104">A função **CreatePropertyDatabase** cria um banco de dados de propriedade que armazena as propriedades de um protocolo.</span><span class="sxs-lookup"><span data-stu-id="afe0e-104">The **CreatePropertyDatabase** function creates a property database that stores the properties of a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe0e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afe0e-105">Syntax</span></span>


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a><span data-ttu-id="afe0e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afe0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afe0e-107">*hProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="afe0e-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afe0e-108">Identificador do protocolo associado ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="afe0e-108">Handle of the protocol that is associated with the database.</span></span> <span data-ttu-id="afe0e-109">Quando Monitor de Rede chama a função de [registro](register-parser.md) , monitor de rede passa o identificador de protocolo para a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="afe0e-109">When Network Monitor calls the [Register](register-parser.md) function, Network Monitor passes the protocol handle to the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="afe0e-110">*nProperties* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="afe0e-110">*nProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afe0e-111">Número de propriedades armazenadas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="afe0e-111">Number of properties stored in the database.</span></span> <span data-ttu-id="afe0e-112">Defina esse parâmetro como o número de propriedades que o protocolo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="afe0e-112">Set this parameter to the number of properties that the protocol supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afe0e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="afe0e-113">Return value</span></span>

<span data-ttu-id="afe0e-114">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="afe0e-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="afe0e-115">Se a função não for bem-sucedida, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="afe0e-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="afe0e-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="afe0e-116">Return code</span></span>                                                                                             | <span data-ttu-id="afe0e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="afe0e-117">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="afe0e-118"><dt>**\_erro interno de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="afe0e-118"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="afe0e-119">Ocorreu um erro interno.</span><span class="sxs-lookup"><span data-stu-id="afe0e-119">An internal error has occurred.</span></span><br/>                                     |
| <dl> <span data-ttu-id="afe0e-120"><dt>**NMERR \_ HPOTOCOL inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="afe0e-120"><dt>**NMERR\_INVALID\_HPOTOCOL**</dt></span></span> </dl> | <span data-ttu-id="afe0e-121">O identificador para o protocolo especificado em *hProtocol* é inválido.</span><span class="sxs-lookup"><span data-stu-id="afe0e-121">The handle to the protocol specified in *hProtocol* is invalid.</span></span><br/>     |
| <dl> <span data-ttu-id="afe0e-122"><dt>**NMERR \_ \_ de \_ memória insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="afe0e-122"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="afe0e-123">Monitor de Rede não tem memória suficiente para criar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="afe0e-123">Network Monitor does not have enough memory to create the database.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="afe0e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="afe0e-124">Remarks</span></span>

<span data-ttu-id="afe0e-125">A função **CreatePropertyDatabase** deve ser chamada somente ao implementar a função [Register](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="afe0e-125">The **CreatePropertyDatabase** function should be called only when implementing the [Register](register-parser.md) function.</span></span> <span data-ttu-id="afe0e-126">O analisador usa **CreatePropertyDatabase** para criar um banco de dados de propriedade que descreve as propriedades de um protocolo.</span><span class="sxs-lookup"><span data-stu-id="afe0e-126">The parser uses **CreatePropertyDatabase** to create a property database that describes the properties of a protocol.</span></span> <span data-ttu-id="afe0e-127">Monitor de Rede usa o banco de dados para interpretar as informações no protocolo.</span><span class="sxs-lookup"><span data-stu-id="afe0e-127">Network Monitor uses the database to interpret the information within the protocol.</span></span>

<span data-ttu-id="afe0e-128">A função **CreatePropertyDatabase** aloca as estruturas que monitor de rede precisa para manter um banco de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="afe0e-128">The **CreatePropertyDatabase** function allocates the structures that Network Monitor needs to maintain a property database.</span></span>

## <a name="requirements"></a><span data-ttu-id="afe0e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afe0e-129">Requirements</span></span>



| <span data-ttu-id="afe0e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="afe0e-130">Requirement</span></span> | <span data-ttu-id="afe0e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="afe0e-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="afe0e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afe0e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="afe0e-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="afe0e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="afe0e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afe0e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="afe0e-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="afe0e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="afe0e-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="afe0e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="afe0e-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="afe0e-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="afe0e-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afe0e-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="afe0e-139"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afe0e-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="afe0e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="afe0e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afe0e-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afe0e-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afe0e-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="afe0e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe0e-143">Registrar</span><span class="sxs-lookup"><span data-stu-id="afe0e-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




