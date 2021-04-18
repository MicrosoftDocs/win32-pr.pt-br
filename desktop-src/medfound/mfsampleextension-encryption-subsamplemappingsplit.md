---
description: Define o mapeamento de sub-amostra para o exemplo que indica os bytes claros e criptografados nos dados de exemplo.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: Atributo MFSampleExtension_Encryption_SubSampleMappingSplit (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105795458"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>Atributo MFSampleExtension de \_ criptografia \_ SubSampleMappingSplit

Define o mapeamento de sub-amostra para o exemplo que indica os bytes claros e criptografados nos dados de exemplo.

## <a name="data-type"></a>Tipo de dados

**BLOB**

## <a name="remarks"></a>Comentários

O **blob** deve conter uma matriz de intervalos de bytes como DWORDs onde cada duas DWORDs faz um conjunto. A primeira DWORD de cada conjunto é o número de bytes claros e a segunda DWORD do conjunto é o número de bytes criptografados. Observe que um par de 0s não é um conjunto válido (ambos os valores podem ser 0, mas não ambos). A matriz de intervalos de bytes indica quais intervalos devem ser descriptografados, incluindo a possibilidade de que o exemplo inteiro não seja descriptografado. É recomendável que isso não seja definido em amostras claras, embora seja possível obter o mesmo resultado definindo-o com os valores apropriados.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir MFSampleExtension de \_ criptografia \_ SubSampleMappingSplit.


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[\_Keyid conteúdo do MFSampleExtension \_](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




