---
description: Exibe uma caixa de diálogo para selecionar certificados e retorna uma coleção desses certificados selecionados.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'Método ICertificates2:: SELECT'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760017"
---
# <a name="icertificates2select-method"></a><span data-ttu-id="28cc8-103">Método ICertificates2:: SELECT</span><span class="sxs-lookup"><span data-stu-id="28cc8-103">ICertificates2::Select method</span></span>

<span data-ttu-id="28cc8-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="28cc8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="28cc8-105">Em vez disso, use a [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="28cc8-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="28cc8-106">O método **Select** exibe uma caixa de diálogo para selecionar certificados e retorna uma coleção desses certificados selecionados.</span><span class="sxs-lookup"><span data-stu-id="28cc8-106">The **Select** method displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span> <span data-ttu-id="28cc8-107">Esse método foi introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="28cc8-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="28cc8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28cc8-108">Syntax</span></span>


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a><span data-ttu-id="28cc8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28cc8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28cc8-110">*Título* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="28cc8-110">*Title* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28cc8-111">Cadeia de caracteres que contém o título da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="28cc8-111">String that contains the title for the dialog box.</span></span> <span data-ttu-id="28cc8-112">O valor padrão é uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="28cc8-112">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="28cc8-113">*DisplayString* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="28cc8-113">*DisplayString* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28cc8-114">Cadeia de caracteres que contém o texto do prompt exibido com a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="28cc8-114">String that contains the prompt text displayed with the dialog box.</span></span> <span data-ttu-id="28cc8-115">O valor padrão é uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="28cc8-115">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="28cc8-116">*bMultiSelect* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="28cc8-116">*bMultiSelect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28cc8-117">Valor booliano que indica se o usuário pode selecionar mais de um certificado.</span><span class="sxs-lookup"><span data-stu-id="28cc8-117">Boolean value that indicates whether the user can select more than one certificate.</span></span> <span data-ttu-id="28cc8-118">Verdadeiro indica que vários certificados podem ser selecionados usando a tecla CTRL ou SHIFT.</span><span class="sxs-lookup"><span data-stu-id="28cc8-118">True indicates multiple certificates can be selected by using the CTRL or SHIFT key.</span></span> <span data-ttu-id="28cc8-119">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="28cc8-119">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28cc8-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28cc8-120">Return value</span></span>

<span data-ttu-id="28cc8-121">Um objeto de [**certificados**](certificates.md) que contém os certificados selecionados na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="28cc8-121">A [**Certificates**](certificates.md) object that contains the certificates selected from the dialog box.</span></span>

<span data-ttu-id="28cc8-122">**Capicom 2,1:** O objeto [**Certificates**](certificates.md) retornado contém referências aos certificados na coleção da qual a seleção foi feita.</span><span class="sxs-lookup"><span data-stu-id="28cc8-122">**CAPICOM 2.1:** The [**Certificates**](certificates.md) object that is returned contains references to the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="28cc8-123">Todas as alterações feitas nos certificados no objeto de **certificados** retornados são refletidas nessa coleção.</span><span class="sxs-lookup"><span data-stu-id="28cc8-123">Any changes made to the certificates in the returned **Certificates** object are reflected in that collection.</span></span>

<span data-ttu-id="28cc8-124">**Capicom 2,0, CApicom 2.0.0.1, CApicom 2.0.0.2 e CApicom 2.0.0.3:** O objeto [**Certificates**](certificates.md) retornado contém cópias dos certificados na coleção da qual a seleção foi feita.</span><span class="sxs-lookup"><span data-stu-id="28cc8-124">**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2, and CAPICOM 2.0.0.3:** The [**Certificates**](certificates.md) object that is returned contains copies of the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="28cc8-125">As alterações feitas nos certificados no objeto de **certificados** retornados não são refletidas nessa coleção.</span><span class="sxs-lookup"><span data-stu-id="28cc8-125">Any changes made to the certificates in the returned **Certificates** object are not reflected in that collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="28cc8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28cc8-126">Requirements</span></span>



| <span data-ttu-id="28cc8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="28cc8-127">Requirement</span></span> | <span data-ttu-id="28cc8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="28cc8-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28cc8-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="28cc8-129">End of client support</span></span><br/> | <span data-ttu-id="28cc8-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28cc8-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="28cc8-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="28cc8-131">End of server support</span></span><br/> | <span data-ttu-id="28cc8-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28cc8-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="28cc8-133">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="28cc8-133">Redistributable</span></span><br/>       | <span data-ttu-id="28cc8-134">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="28cc8-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="28cc8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="28cc8-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="28cc8-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28cc8-136"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
