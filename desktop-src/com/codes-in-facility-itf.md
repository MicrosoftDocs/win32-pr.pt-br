---
title: Códigos em FACILITY_ITF
description: Códigos no FACILITy \_ ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916107"
---
# <a name="codes-in-facility_itf"></a><span data-ttu-id="da767-103">Códigos no FACILITy \_ ITF</span><span class="sxs-lookup"><span data-stu-id="da767-103">Codes in FACILITY\_ITF</span></span>

<span data-ttu-id="da767-104">**HRESULT** s com instalações como a instalação \_ nula e o \_ RPC de instalação têm um significado universal porque eles são definidos em uma única fonte: Microsoft.</span><span class="sxs-lookup"><span data-stu-id="da767-104">**HRESULT** s with facilities such as FACILITY\_NULL and FACILITY\_RPC have universal meaning because they are defined at a single source: Microsoft.</span></span> <span data-ttu-id="da767-105">No entanto, **HRESULT** s no recurso \_ ITF são determinados pelo método de função ou de interface do qual eles são retornados.</span><span class="sxs-lookup"><span data-stu-id="da767-105">However, **HRESULT** s in FACILITY\_ITF are determined by the function or interface method from which they are returned.</span></span> <span data-ttu-id="da767-106">Isso significa que o mesmo valor de 32 bits no recurso \_ ITF retornado de dois métodos de interface diferentes pode ter significados diferentes.</span><span class="sxs-lookup"><span data-stu-id="da767-106">This means that the same 32-bit value in FACILITY\_ITF returned from two different interface methods might have different meanings.</span></span>

<span data-ttu-id="da767-107">O motivo pelo qual o **HRESULT** s no recurso \_ ITF pode ter significados diferentes em interfaces diferentes é que **HRESULT** s é mantido para um tamanho de tipo de dados eficiente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="da767-107">The reason **HRESULT** s in FACILITY\_ITF can have different meanings in different interfaces is that **HRESULT** s are kept to an efficient data type size of 32 bits.</span></span> <span data-ttu-id="da767-108">Infelizmente, 32 bits não é grande o suficiente para o desenvolvimento de um sistema de alocação de código de erro que evita códigos conflitantes alocados por programadores diferentes em momentos diferentes em locais diferentes (ao contrário da manipulação de identificadores de interface e CLSIDs).</span><span class="sxs-lookup"><span data-stu-id="da767-108">Unfortunately, 32 bits is not large enough for the development of an error code allocation system that avoids conflicting codes allocated by different programmers at different times in different places (unlike the handling of interface identifiers and CLSIDs).</span></span> <span data-ttu-id="da767-109">Como resultado, o **HRESULT** de 32 bits é estruturado de forma que a Microsoft possa definir vários códigos de erro universal, permitindo que outros programadores definam novos códigos de erro sem medo de conflito.</span><span class="sxs-lookup"><span data-stu-id="da767-109">As a result, the 32-bit **HRESULT** is structured such that Microsoft can define several universal error codes, while allowing other programmers to define new error codes without fear of conflict.</span></span> <span data-ttu-id="da767-110">A Convenção de código de status é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="da767-110">The status code convention is as follows:</span></span>

-   <span data-ttu-id="da767-111">Os códigos de status em instalações diferentes do recurso \_ ITF podem ser definidos somente pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="da767-111">Status codes in facilities other than FACILITY\_ITF can be defined only by Microsoft.</span></span>
-   <span data-ttu-id="da767-112">Os códigos de status no recurso de instalação \_ ITF são definidos exclusivamente pelo desenvolvedor da interface ou função que retorna o código de status.</span><span class="sxs-lookup"><span data-stu-id="da767-112">Status codes in facility FACILITY\_ITF are defined solely by the developer of the interface or function that returns the status code.</span></span> <span data-ttu-id="da767-113">Para evitar códigos de erro conflitantes, qualquer pessoa que define a interface é responsável por coordenar e publicar os \_ códigos de status ITF de instalação associados a essa interface.</span><span class="sxs-lookup"><span data-stu-id="da767-113">To avoid conflicting error codes, whoever defines the interface is responsible for coordinating and publishing the FACILITY\_ITF status codes associated with that interface.</span></span>

<span data-ttu-id="da767-114">Todos os códigos de ITF de instalações definidos COM \_ têm um valor de código no intervalo de 0x0000-0x01FF.</span><span class="sxs-lookup"><span data-stu-id="da767-114">All the COM-defined FACILITY\_ITF codes have a code value in the range of 0x0000-0x01FF.</span></span> <span data-ttu-id="da767-115">Embora seja legal usar qualquer código no recurso \_ ITF, é recomendável que apenas os valores de código no intervalo de 0x0200-0xFFFF sejam usados.</span><span class="sxs-lookup"><span data-stu-id="da767-115">While it is legal to use any codes in FACILITY\_ITF, it is recommended that only code values in the range of 0x0200-0xFFFF be used.</span></span> <span data-ttu-id="da767-116">Essa recomendação é feita como um meio de reduzir a confusão com erros definidos COM.</span><span class="sxs-lookup"><span data-stu-id="da767-116">This recommendation is made as a means of reducing confusion with any COM-defined errors.</span></span>

<span data-ttu-id="da767-117">Também é recomendável que os desenvolvedores definam novas funções e interfaces para retornar códigos de erro, conforme definido pelo COM e em instalações diferentes do recurso \_ ITF.</span><span class="sxs-lookup"><span data-stu-id="da767-117">It is also recommended that developers define new functions and interfaces to return error codes as defined by COM and in facilities other than FACILITY\_ITF.</span></span> <span data-ttu-id="da767-118">Em particular, as interfaces que têm qualquer chance de serem remotas usando RPC no futuro devem definir os códigos de RPC do recurso \_ como válidos.</span><span class="sxs-lookup"><span data-stu-id="da767-118">In particular, interfaces that have any chance of being remoted using RPC in the future should define the FACILITY\_RPC codes as legal.</span></span> <span data-ttu-id="da767-119">E \_ inesperado é um código de erro específico que a maioria dos desenvolvedores deseja tornar universalmente legal.</span><span class="sxs-lookup"><span data-stu-id="da767-119">E\_UNEXPECTED is a specific error code that most developers will want to make universally legal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da767-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da767-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da767-121">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="da767-121">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




