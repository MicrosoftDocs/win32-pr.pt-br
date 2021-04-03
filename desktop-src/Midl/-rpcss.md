---
title: comutador/RPCSS
description: A opção/RPCSS, quando especificada, atua como se o atributo de alocação de habilitação \_ fosse especificado em todas as operações da interface. O uso desse atributo não é recomendado.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- MIDL do comutador/RPCSS
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006394"
---
# <a name="rpcss-switch"></a><span data-ttu-id="af596-105">comutador/RPCSS</span><span class="sxs-lookup"><span data-stu-id="af596-105">/rpcss switch</span></span>

<span data-ttu-id="af596-106">A opção **/RPCSS** , quando especificada, atua como se o atributo de [**\_ alocação de habilitação**](enable-allocate.md) fosse especificado em todas as operações da interface.</span><span class="sxs-lookup"><span data-stu-id="af596-106">The **/rpcss** switch, when specified, acts as though the [**enable\_allocate**](enable-allocate.md) attribute was specified on all operations of the interface.</span></span> <span data-ttu-id="af596-107">O uso desse atributo não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="af596-107">The usage of this attribute is not recommended.</span></span>

``` syntax
midl /rpcss
```

## <a name="switch-options"></a><span data-ttu-id="af596-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="af596-108">Switch Options</span></span>

<span data-ttu-id="af596-109">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="af596-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="af596-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="af596-110">Remarks</span></span>

<span data-ttu-id="af596-111">No modo padrão, o pacote RpcSs será habilitado somente se o procedimento ou a interface tiver o atributo [**habilitar \_ alocação**](enable-allocate.md) ou o comutador **/RPCSS** for especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="af596-111">In default mode, the RpcSs package is enabled only if either the procedure or interface has the [**enable\_allocate**](enable-allocate.md) attribute or the **/rpcss** switch is specified on the command line.</span></span> <span data-ttu-id="af596-112">No modo **/OSF** , o stub do lado do servidor habilita o pacote de alocação do RPCSS.</span><span class="sxs-lookup"><span data-stu-id="af596-112">In **/osf** mode, the server-side stub enables the RpcSs allocation package.</span></span>

## <a name="examples"></a><span data-ttu-id="af596-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="af596-113">Examples</span></span>

<span data-ttu-id="af596-114">**MIDL/RPCSS filename. idl**</span><span class="sxs-lookup"><span data-stu-id="af596-114">**midl /rpcss filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="af596-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="af596-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af596-116">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="af596-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="af596-117">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="af596-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="af596-118">**Habilitar \_ alocação**</span><span class="sxs-lookup"><span data-stu-id="af596-118">**enable\_allocate**</span></span>](enable-allocate.md)
</dt> <dt>

[<span data-ttu-id="af596-119">**/osf**</span><span class="sxs-lookup"><span data-stu-id="af596-119">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




