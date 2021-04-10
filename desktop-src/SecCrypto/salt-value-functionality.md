---
description: O provedor de base cria chaves simétricas de 40 bits criadas com onze bytes de Salt de zero valor, onze bytes de Salt diferente de zero se cript. \_ Create \_ Salt for especificado ou nenhum valor de Salt.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Funcionalidade de valor de Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296518"
---
# <a name="salt-value-functionality"></a><span data-ttu-id="f81b2-103">Funcionalidade de valor de Salt</span><span class="sxs-lookup"><span data-stu-id="f81b2-103">Salt Value Functionality</span></span>

<span data-ttu-id="f81b2-104">O provedor de base cria [*chaves simétricas*](../secgloss/s-gly.md) de 40 bits criadas com onze bytes de [*Salt*](../secgloss/s-gly.md)de zero valor, onze bytes de Salt diferente de zero se cript. \_ Create \_ Salt for especificado ou nenhum valor de Salt.</span><span class="sxs-lookup"><span data-stu-id="f81b2-104">The Base Provider creates 40-bit [*symmetric keys*](../secgloss/s-gly.md) created with eleven bytes of zero-value [*salt*](../secgloss/s-gly.md), eleven bytes of nonzero salt if CRYPT\_CREATE\_SALT is specified, or no salt value.</span></span> <span data-ttu-id="f81b2-105">No entanto, uma chave simétrica de 40 bits com Salt de valor zero não é equivalente a uma chave simétrica de 40 bits sem Salt.</span><span class="sxs-lookup"><span data-stu-id="f81b2-105">A 40-bit symmetric key with zero-value salt, however, is not equivalent to a 40-bit symmetric key without salt.</span></span> <span data-ttu-id="f81b2-106">Para interoperabilidade, as chaves devem ser criadas sem Salt.</span><span class="sxs-lookup"><span data-stu-id="f81b2-106">For interoperability, keys must be created without salt.</span></span> <span data-ttu-id="f81b2-107">Esse problema resulta de uma condição padrão que ocorre apenas com chaves de exatamente 40 bits.</span><span class="sxs-lookup"><span data-stu-id="f81b2-107">This problem results from a default condition that occurs only with keys of exactly 40 bits.</span></span> <span data-ttu-id="f81b2-108">Todos os outros [*comprimentos de chave*](../secgloss/k-gly.md) não têm Salt alocado por padrão.</span><span class="sxs-lookup"><span data-stu-id="f81b2-108">All other [*key lengths*](../secgloss/k-gly.md) do not have salt allocated by default.</span></span>

<span data-ttu-id="f81b2-109">Tanto os provedores de base quanto o provedor estendido podem usar o \_ sinalizador de Salt não criptografado \_ para especificar que nenhum valor de Salt seja alocado para uma chave simétrica de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="f81b2-109">Both the Base Providers and the Extended Provider can use the CRYPT\_NO\_SALT flag to specify that no salt value is allocated for a 40-bit symmetric key.</span></span> <span data-ttu-id="f81b2-110">As funções que aceitam esse sinalizador são [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="f81b2-110">The functions that accept this flag are [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey), and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="f81b2-111">Por padrão, essas funções fornecem compatibilidade com versões anteriores para o caso de chave simétrica de 40 bits, continuando o uso do Salt de onze bytes de valor zero.</span><span class="sxs-lookup"><span data-stu-id="f81b2-111">By default, these functions provide backward compatibility for the 40-bit symmetric key case by continuing the use of the eleven-byte-long zero-value salt.</span></span>

 

 
