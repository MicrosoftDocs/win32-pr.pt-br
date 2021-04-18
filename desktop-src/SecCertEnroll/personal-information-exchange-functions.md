---
description: Cada uma das seções a seguir discute uma função exportada por Xenroll.dll para gerenciar mensagens de troca de informações pessoais (PFX).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funções de troca de informações pessoais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760023"
---
# <a name="personal-information-exchange-functions"></a><span data-ttu-id="22714-103">Funções de troca de informações pessoais</span><span class="sxs-lookup"><span data-stu-id="22714-103">Personal Information Exchange Functions</span></span>

<span data-ttu-id="22714-104">Cada uma das seções a seguir discute uma função exportada por Xenroll.dll para gerenciar mensagens de troca de informações pessoais (PFX).</span><span class="sxs-lookup"><span data-stu-id="22714-104">Each of the following sections discusses a function exported by Xenroll.dll to manage Personal Information Exchange (PFX) messages.</span></span> <span data-ttu-id="22714-105">Cada seção também aborda como usar CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="22714-105">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="createfilepfxwstr"></a><span data-ttu-id="22714-106">createFilePFXWStr</span><span class="sxs-lookup"><span data-stu-id="22714-106">createFilePFXWStr</span></span>

<span data-ttu-id="22714-107">A função [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) no Xenroll.dll salva uma cadeia de certificados e uma [*chave privada*](/windows/desktop/SecGloss/p-gly) em um arquivo usando o formato PFX.</span><span class="sxs-lookup"><span data-stu-id="22714-107">The [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) function in Xenroll.dll saves a certificate chain and [*private key*](/windows/desktop/SecGloss/p-gly) in a file by using the PFX format.</span></span>

<span data-ttu-id="22714-108">A biblioteca de CertEnroll.dll não implementa diretamente a funcionalidade para copiar a mensagem PFX em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="22714-108">The CertEnroll.dll library does not directly implement functionality to copy the PFX message to a file.</span></span> <span data-ttu-id="22714-109">No entanto, você pode usar o método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) na interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para criar uma mensagem pfx codificada e gravar uma função personalizada para salvar a mensagem em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="22714-109">You can, however, use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message and write a custom function to save the message in a file.</span></span>

## <a name="createpfxwstr"></a><span data-ttu-id="22714-110">createPFXWStr</span><span class="sxs-lookup"><span data-stu-id="22714-110">createPFXWStr</span></span>

<span data-ttu-id="22714-111">A função [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) no Xenroll.dll salva uma cadeia de certificados e uma chave privada em uma cadeia de caracteres de formato PFX.</span><span class="sxs-lookup"><span data-stu-id="22714-111">The [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) function in Xenroll.dll saves a certificate chain and private key in a PFX format string.</span></span>

<span data-ttu-id="22714-112">Você pode usar o método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) na interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para criar uma mensagem pfx codificada que contém a cadeia de certificados e a chave.</span><span class="sxs-lookup"><span data-stu-id="22714-112">You can use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message that contains the certificate chain and key.</span></span> <span data-ttu-id="22714-113">Você pode especificar uma senha, opções de exportação e tipo de codificação.</span><span class="sxs-lookup"><span data-stu-id="22714-113">You can specify a password, export options, and encoding type.</span></span> <span data-ttu-id="22714-114">Para recuperar uma cadeia de caracteres equivalente à retornada de [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), passe o \_ \_ sinalizador binário de cadeia de caracteres cript XCN \_ no parâmetro de *codificação* do método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .</span><span class="sxs-lookup"><span data-stu-id="22714-114">To retrieve a string that is equivalent to that returned from [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pass the XCN\_CRYPT\_STRING\_BINARY flag in the in the *Encoding* parameter of the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22714-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22714-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22714-116">Mapeando Xenroll.dll para CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="22714-116">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="22714-117">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="22714-117">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
