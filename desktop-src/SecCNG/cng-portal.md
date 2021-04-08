---
description: A CNG é uma API de criptografia que você pode usar para criar um software de segurança de criptografia para gerenciamento de chaves de criptografia, criptografia e segurança de dados, criptografia e segurança de rede.
ms.assetid: eaad88a1-4e1d-4246-9560-8eef60f8b70f
title: 'API de criptografia: próxima geração'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d485f8371905961c63fbab66b29d0db544e3271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826767"
---
# <a name="cryptography-api-next-generation"></a><span data-ttu-id="b7107-103">API de criptografia: próxima geração</span><span class="sxs-lookup"><span data-stu-id="b7107-103">Cryptography API: Next Generation</span></span>

## <a name="purpose"></a><span data-ttu-id="b7107-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="b7107-104">Purpose</span></span>

<span data-ttu-id="b7107-105">Cryptography API: CNG (próxima geração) é a substituição de longo prazo para o [*CryptoAPI*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b7107-105">Cryptography API: Next Generation (CNG) is the long-term replacement for the [*CryptoAPI*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="b7107-106">A CNG foi projetada para ser extensível em muitos níveis e a criptografia não é um comportamento diferente.</span><span class="sxs-lookup"><span data-stu-id="b7107-106">CNG is designed to be extensible at many levels and cryptography agnostic in behavior.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b7107-107">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="b7107-107">Developer audience</span></span>

<span data-ttu-id="b7107-108">A CNG destina-se ao uso por desenvolvedores de aplicativos que permitirão que os usuários criem e troquem documentos e outros dados em um ambiente seguro, especialmente em mídias não seguras, como a Internet.</span><span class="sxs-lookup"><span data-stu-id="b7107-108">CNG is intended for use by developers of applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="b7107-109">Os desenvolvedores devem estar familiarizados com as linguagens de programação C e C++ e com o ambiente de programação baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="b7107-109">Developers should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="b7107-110">Embora não seja necessário, uma compreensão de criptografia ou de assuntos relacionados à segurança é aconselhada.</span><span class="sxs-lookup"><span data-stu-id="b7107-110">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="b7107-111">Se você estiver desenvolvendo um provedor de algoritmo de criptografia CNG ou um provedor de armazenamento de chaves, baixe o [Kit de desenvolvimento do provedor criptográfico](https://www.microsoft.com/download/details.aspx?id=30688) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7107-111">If you are developing a CNG cryptographic algorithm provider or key storage provider, you must download the [Cryptographic Provider Development Kit](https://www.microsoft.com/download/details.aspx?id=30688) from Microsoft.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b7107-112">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="b7107-112">Run-time requirements</span></span>

<span data-ttu-id="b7107-113">A CNG tem suporte a partir do Windows Server 2008 e do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b7107-113">CNG is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="b7107-114">Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="b7107-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b7107-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b7107-115">In this section</span></span>



| <span data-ttu-id="b7107-116">Tópico</span><span class="sxs-lookup"><span data-stu-id="b7107-116">Topic</span></span>                                         | <span data-ttu-id="b7107-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7107-117">Description</span></span>                                                                                                                                    |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7107-118">Sobre a CNG</span><span class="sxs-lookup"><span data-stu-id="b7107-118">About CNG</span></span>](about-cng.md)<br/>         | <span data-ttu-id="b7107-119">Descreve recursos da CNG, primitivos de criptografia e armazenamento de chave, recuperação, importação e exportação.</span><span class="sxs-lookup"><span data-stu-id="b7107-119">Describes CNG features, cryptographic primitives, and key storage, retrieval, import, and export.</span></span><br/>                                   |
| [<span data-ttu-id="b7107-120">Usando o CNG</span><span class="sxs-lookup"><span data-stu-id="b7107-120">Using CNG</span></span>](using-cng.md)<br/>         | <span data-ttu-id="b7107-121">Explica como usar os recursos de configuração de criptografia da CNG e da programação CNG típica.</span><span class="sxs-lookup"><span data-stu-id="b7107-121">Explains how to use the cryptography configuration features of CNG and typical CNG programming.</span></span><br/>                                     |
| [<span data-ttu-id="b7107-122">Referência CNG</span><span class="sxs-lookup"><span data-stu-id="b7107-122">CNG Reference</span></span>](cng-reference.md)<br/> | <span data-ttu-id="b7107-123">Descrições detalhadas dos elementos de programação da CNG.</span><span class="sxs-lookup"><span data-stu-id="b7107-123">Detailed descriptions of the CNG programming elements.</span></span> <span data-ttu-id="b7107-124">Essas páginas incluem descrições de referência da API para trabalhar com a CNG.</span><span class="sxs-lookup"><span data-stu-id="b7107-124">These pages include reference descriptions of the API for working with CNG.</span></span> <br/> |



 

 

