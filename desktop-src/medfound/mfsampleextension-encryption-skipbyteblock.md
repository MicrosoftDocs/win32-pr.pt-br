---
description: Especifica o tamanho do bloco de bytes claro (não criptografado) para criptografia de padrão baseada em exemplo.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: Atributo MFSampleExtension_Encryption_SkipByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18003c03df7e65314846d34cb1d1093f5b2507a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827815"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a><span data-ttu-id="60ddc-103">Atributo MFSampleExtension de \_ criptografia \_ SkipByteBlock</span><span class="sxs-lookup"><span data-stu-id="60ddc-103">MFSampleExtension\_Encryption\_SkipByteBlock attribute</span></span>

<span data-ttu-id="60ddc-104">Especifica o tamanho do bloco de bytes claro (não criptografado) para criptografia de padrão baseada em exemplo.</span><span class="sxs-lookup"><span data-stu-id="60ddc-104">Specifies the clear (non-encrypted) byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="60ddc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="60ddc-105">Data type</span></span>

<span data-ttu-id="60ddc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="60ddc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="60ddc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="60ddc-107">Remarks</span></span>

<span data-ttu-id="60ddc-108">O número de bytes criptografados no bloco de mapeamento de subamostras é especificado no atributo [MFSampleExtension de \_ criptografia \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) .</span><span class="sxs-lookup"><span data-stu-id="60ddc-108">The number of encrypted bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) attribute.</span></span> <span data-ttu-id="60ddc-109">Se um desses atributos não estiver presente ou tiver um valor de 0, significa que os dados de exemplo não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="60ddc-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="60ddc-110">Ambos os valores devem ser diferentes de zero, valores positivos ou ambos devem ter um valor igual a zero.</span><span class="sxs-lookup"><span data-stu-id="60ddc-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="60ddc-111">Nos casos em que a origem é baseada em MP4, o valor é definido com base nos valores do \_ bloco de ignorar \_ bytes padrão \_ dentro da caixa rastrear criptografia (' tenc ') no cabeçalho MP4.</span><span class="sxs-lookup"><span data-stu-id="60ddc-111">In cases where the Source is MP4-based, the value is set based off the values of default\_skip\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="60ddc-112">Para obter mais informações, consulte [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span><span class="sxs-lookup"><span data-stu-id="60ddc-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60ddc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60ddc-113">Requirements</span></span>



| <span data-ttu-id="60ddc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="60ddc-114">Requirement</span></span> | <span data-ttu-id="60ddc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="60ddc-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60ddc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60ddc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="60ddc-117">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="60ddc-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="60ddc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60ddc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="60ddc-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="60ddc-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="60ddc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60ddc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="60ddc-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60ddc-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




