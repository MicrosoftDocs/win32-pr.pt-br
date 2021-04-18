---
title: função glGetPointerv (GL. h)
description: A função glGetPointerv retorna o endereço de uma matriz de dados de vértice.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- função glGetPointerv OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794438"
---
# <a name="glgetpointerv-function"></a><span data-ttu-id="34e4e-104">função glGetPointerv</span><span class="sxs-lookup"><span data-stu-id="34e4e-104">glGetPointerv function</span></span>

<span data-ttu-id="34e4e-105">A função **glGetPointerv** retorna o endereço de uma matriz de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="34e4e-105">The **glGetPointerv** function returns the address of a vertex data array.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e4e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34e4e-106">Syntax</span></span>


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a><span data-ttu-id="34e4e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34e4e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e4e-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="34e4e-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="34e4e-109">O tipo de ponteiro de matriz a ser retornado das seguintes constantes simbólicas: o ponteiro da matriz de cores GL, o indicador de borda do GL Flag, o ponteiro do buffer de comentários do GL, o ponteiro da matriz de índice GL, o ponteiro de matriz normal do GL, o ponteiro de \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ matriz coord de textura GL, o marcador de \_ buffer de \_ \_ \_ seleção GL e o \_ \_ \_ \_ \_ ponteiro</span><span class="sxs-lookup"><span data-stu-id="34e4e-109">The type of array pointer to return from the following symbolic constants: GL\_COLOR\_ARRAY\_POINTER, GL\_EDGE\_FLAG\_ARRAY\_POINTER, GL\_FEEDBACK\_BUFFER\_POINTER, GL\_INDEX\_ARRAY\_POINTER, GL\_NORMAL\_ARRAY\_POINTER, GL\_TEXTURE\_COORD\_ARRAY\_POINTER, GL\_SELECTION\_BUFFER\_POINTER, and GL\_VERTEX\_ARRAY\_POINTER.</span></span>

</dd> <dt>

<span data-ttu-id="34e4e-110">*params*</span><span class="sxs-lookup"><span data-stu-id="34e4e-110">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="34e4e-111">Retorna o valor do ponteiro de matriz especificado por *pname*.</span><span class="sxs-lookup"><span data-stu-id="34e4e-111">Returns the value of the array pointer specified by *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e4e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34e4e-112">Return value</span></span>

<span data-ttu-id="34e4e-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="34e4e-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="34e4e-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="34e4e-114">Error codes</span></span>

<span data-ttu-id="34e4e-115">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="34e4e-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="34e4e-116">Nome</span><span class="sxs-lookup"><span data-stu-id="34e4e-116">Name</span></span>                                                                                             | <span data-ttu-id="34e4e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="34e4e-117">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="34e4e-118"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="34e4e-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="34e4e-119">*pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="34e4e-119">*pname* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="34e4e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="34e4e-120">Remarks</span></span>

<span data-ttu-id="34e4e-121">A função **glGetPointerv** retorna informações de ponteiro de matriz.</span><span class="sxs-lookup"><span data-stu-id="34e4e-121">The **glGetPointerv** function returns array pointer information.</span></span> <span data-ttu-id="34e4e-122">O parâmetro *pname* é uma constante simbólica que especifica o tipo de ponteiro de matriz a ser retornado, e *params* é um ponteiro para um local para inserir os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="34e4e-122">The *pname* parameter is a symbolic constant specifying the kind of array pointer to return, and *params* is a pointer to a location to place the returned data.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e4e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34e4e-123">Requirements</span></span>



| <span data-ttu-id="34e4e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="34e4e-124">Requirement</span></span> | <span data-ttu-id="34e4e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="34e4e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34e4e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34e4e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="34e4e-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="34e4e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="34e4e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34e4e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="34e4e-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="34e4e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34e4e-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="34e4e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="34e4e-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="34e4e-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="34e4e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34e4e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="34e4e-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34e4e-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="34e4e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="34e4e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34e4e-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34e4e-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34e4e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="34e4e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e4e-137">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="34e4e-137">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="34e4e-138">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="34e4e-138">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="34e4e-139">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="34e4e-139">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="34e4e-140">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="34e4e-140">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="34e4e-141">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="34e4e-141">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="34e4e-142">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="34e4e-142">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="34e4e-143">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="34e4e-143">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="34e4e-144">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="34e4e-144">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="34e4e-145">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="34e4e-145">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





