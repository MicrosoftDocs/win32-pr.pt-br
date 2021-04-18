---
description: As \_ constantes de sinalizador de bit LINEADDRESSMODE descrevem várias maneiras de identificar um endereço em um dispositivo de linha.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: Constantes de LINEADDRESSMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810460"
---
# <a name="lineaddressmode_-constants"></a><span data-ttu-id="55f18-103">\_Constantes LINEADDRESSMODE</span><span class="sxs-lookup"><span data-stu-id="55f18-103">LINEADDRESSMODE\_ Constants</span></span>

<span data-ttu-id="55f18-104">As constantes de sinalizador de bit **LINEADDRESSMODE \_** descrevem várias maneiras de identificar um endereço em um dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="55f18-104">The **LINEADDRESSMODE\_** bit-flag constants describe various ways of identifying an address on a line device.</span></span>

<dl> <dt>

<span data-ttu-id="55f18-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ AddressID**</span><span class="sxs-lookup"><span data-stu-id="55f18-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE\_ADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55f18-106">O endereço é especificado com um pequeno inteiro no intervalo de 0 a *dwNumAddresses* menos um, em que *dwNumAddresses* é o valor nos recursos do dispositivo da linha.</span><span class="sxs-lookup"><span data-stu-id="55f18-106">The address is specified with a small integer in the range 0 to *dwNumAddresses* minus one, where *dwNumAddresses* is the value in the line's device capabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55f18-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**</span><span class="sxs-lookup"><span data-stu-id="55f18-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE\_DIALABLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55f18-108">O endereço é especificado por meio de seu número de telefone.</span><span class="sxs-lookup"><span data-stu-id="55f18-108">The address is specified through its phone number.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55f18-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="55f18-109">Remarks</span></span>

<span data-ttu-id="55f18-110">Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55f18-110">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="55f18-111">Os 16 bits de ordem inferior são reservados.</span><span class="sxs-lookup"><span data-stu-id="55f18-111">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="55f18-112">Essa constante é usada para selecionar um endereço em uma linha na qual uma chamada deve ser originada.</span><span class="sxs-lookup"><span data-stu-id="55f18-112">This constant is used to select an address on a line on which to originate a call.</span></span> <span data-ttu-id="55f18-113">O modelo usual selecionaria o endereço por meio de seu identificador de endereço.</span><span class="sxs-lookup"><span data-stu-id="55f18-113">The usual model would select the address by means of its address identifier.</span></span> <span data-ttu-id="55f18-114">Identificadores de endereço são o mecanismo usado para identificar endereços em toda a TAPI.</span><span class="sxs-lookup"><span data-stu-id="55f18-114">Address identifiers are the mechanism used to identify addresses throughout TAPI.</span></span> <span data-ttu-id="55f18-115">No entanto, em alguns ambientes, ao fazer uma chamada, geralmente é mais prático identificar o endereço de origem de uma chamada por número de telefone em vez de pelo identificador de endereço.</span><span class="sxs-lookup"><span data-stu-id="55f18-115">However, in some environments, when making a call, it is often more practical to identify a call's originating address by phone number rather than by address identifier.</span></span> <span data-ttu-id="55f18-116">Um exemplo é a possível modelagem de um grande número de estações (terceiros) no comutador por meio de um dispositivo de linha com muitos endereços.</span><span class="sxs-lookup"><span data-stu-id="55f18-116">One example is in the possible modeling of large numbers of stations (third party) on the switch by means of one line device with many addresses.</span></span> <span data-ttu-id="55f18-117">A linha representa o conjunto de todas as estações e cada estação é mapeada para um endereço com seu próprio número de telefone principal e identificador de endereço.</span><span class="sxs-lookup"><span data-stu-id="55f18-117">The line represents the set of all stations, and each station is mapped to an address with its own primary phone number and address identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f18-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55f18-118">Requirements</span></span>



| <span data-ttu-id="55f18-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="55f18-119">Requirement</span></span> | <span data-ttu-id="55f18-120">Valor</span><span class="sxs-lookup"><span data-stu-id="55f18-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="55f18-121">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="55f18-121">TAPI version</span></span><br/> | <span data-ttu-id="55f18-122">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="55f18-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="55f18-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55f18-123">Header</span></span><br/>       | <dl> <span data-ttu-id="55f18-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="55f18-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




