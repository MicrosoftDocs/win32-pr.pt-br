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
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a>Atributo MFSampleExtension de \_ criptografia \_ SkipByteBlock

Especifica o tamanho do bloco de bytes claro (não criptografado) para criptografia de padrão baseada em exemplo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O número de bytes criptografados no bloco de mapeamento de subamostras é especificado no atributo [MFSampleExtension de \_ criptografia \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) . Se um desses atributos não estiver presente ou tiver um valor de 0, significa que os dados de exemplo não são criptografados. Ambos os valores devem ser diferentes de zero, valores positivos ou ambos devem ter um valor igual a zero.

Nos casos em que a origem é baseada em MP4, o valor é definido com base nos valores do \_ bloco de ignorar \_ bytes padrão \_ dentro da caixa rastrear criptografia (' tenc ') no cabeçalho MP4. Para obter mais informações, consulte [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 




