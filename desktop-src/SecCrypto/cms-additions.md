---
description: A sintaxe de mensagem de criptografia (CMS), derivada da \# versão 1,5 do PKCS 7, é a sintaxe usada para fazer hash, assinar digitalmente, autenticar e criptografar mensagens arbitrárias.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Adições de CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753927"
---
# <a name="cms-additions"></a><span data-ttu-id="1846e-103">Adições de CMS</span><span class="sxs-lookup"><span data-stu-id="1846e-103">CMS Additions</span></span>

<span data-ttu-id="1846e-104">A sintaxe de mensagem de criptografia (CMS), derivada da \# versão 1,5 do PKCS 7, é a sintaxe usada para fazer [*hash*](../secgloss/h-gly.md), [*assinar digitalmente*](../secgloss/d-gly.md), autenticar e criptografar mensagens arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="1846e-104">Cryptographic Message Syntax (CMS), derived from PKCS \#7 version 1.5, is the syntax used to [*hash*](../secgloss/h-gly.md), [*digitally sign*](../secgloss/d-gly.md), authenticate, and encrypt arbitrary messages.</span></span> <span data-ttu-id="1846e-105">Sempre que possível, a compatibilidade com versões anteriores é preservada; no entanto, foram feitas alterações para acomodar a transferência de certificado de atributo e técnicas de contrato de chave para o gerenciamento de chaves.</span><span class="sxs-lookup"><span data-stu-id="1846e-105">Where possible, backward compatibility is preserved; however, changes have been made to accommodate attribute certificate transfer and key agreement techniques for key management.</span></span> <span data-ttu-id="1846e-106">O CMS permite vários encapsulamentos para que um envelope de encapsulamento possa ser aninhado dentro de outro.</span><span class="sxs-lookup"><span data-stu-id="1846e-106">CMS allows multiple encapsulation so that one encapsulation envelope can be nested inside another.</span></span> <span data-ttu-id="1846e-107">Além disso, uma parte pode assinar digitalmente os dados encapsulados anteriormente; atributos arbitrários, como o tempo de assinatura, podem ser assinados junto com o conteúdo da mensagem; atributos e, como [*referendas*](../secgloss/c-gly.md), podem ser associados a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="1846e-107">Also, one party can digitally sign previously encapsulated data; arbitrary attributes, such as signing time, can be signed along with the message content; and attributes, such as [*countersignatures*](../secgloss/c-gly.md), can be associated with a signature.</span></span> <span data-ttu-id="1846e-108">O CMS pode dar suporte a várias arquiteturas para o gerenciamento de chaves baseado em certificado.</span><span class="sxs-lookup"><span data-stu-id="1846e-108">CMS can support a variety of architectures for certificate-based key management.</span></span>

<span data-ttu-id="1846e-109">Para dar suporte a recursos adicionais do CMS, as estruturas de dados subjacentes receberam novos campos.</span><span class="sxs-lookup"><span data-stu-id="1846e-109">To support additional CMS capabilities, underlying data structures have been given new fields.</span></span> <span data-ttu-id="1846e-110">Novos sinalizadores e valores de parâmetros também foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="1846e-110">New flags and parameter values have also been added.</span></span> <span data-ttu-id="1846e-111">Todas as estruturas de dados e todas as APIs que usam o CMS são compatíveis com 100% de compatibilidade com PKCS \# 7 versão 1,5.</span><span class="sxs-lookup"><span data-stu-id="1846e-111">All data structures and all APIs using CMS are 100 percent backward compatible with PKCS \#7 version 1.5.</span></span>

<span data-ttu-id="1846e-112">As adições incluem [adições de dados envelopadas](enveloped-data-additions.md) e [adições de dados assinadas](signed-data-additions.md).</span><span class="sxs-lookup"><span data-stu-id="1846e-112">Additions include [Enveloped Data Additions](enveloped-data-additions.md) and [Signed Data Additions](signed-data-additions.md).</span></span>

 

 
