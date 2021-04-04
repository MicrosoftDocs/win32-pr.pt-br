---
description: Especifica o tamanho do bloco de bytes criptografados para a criptografia de padrão baseada em exemplo.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: Atributo MFSampleExtension_Encryption_CryptByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010806"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>Atributo MFSampleExtension de \_ criptografia \_ CryptByteBlock

Especifica o tamanho do bloco de bytes criptografados para a criptografia de padrão baseada em exemplo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O número de bytes claros (não criptografados) no bloco de mapeamento de subamostras são especificados no atributo [MFSampleExtension de \_ criptografia \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) . Se um desses atributos não estiver presente ou tiver um valor de 0, significa que os dados de exemplo não são criptografados. Ambos os valores devem ser diferentes de zero, valores positivos ou ambos devem ter um valor igual a zero.

Nos casos em que a origem é baseada em MP4, o valor é definido com base nos valores do \_ bloco de bytes criptografados padrão \_ \_ dentro da caixa rastrear criptografia (' tenc ') no cabeçalho MP4. Para obter mais informações, consulte [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 




