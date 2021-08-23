---
description: Especifica se o aplicativo requer suporte ao Microsoft Direct3D no leitor de origem ou no gravador de coletor.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: Atributo MF_READWRITE_D3D_OPTIONAL (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cebc24991e5c2bfb90b7153f3a90a2e7447c2daef987b2956680e89f162223ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664106"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>\_ \_ Atributo opcional MF ReadWrite D3D \_

Especifica se o aplicativo requer suporte ao Microsoft Direct3D no [leitor de origem](source-reader.md) ou no [gravador de coletor](sink-writer.md).

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplicará somente se o aplicativo habilitar o suporte a Direct3D usando o atributo de [ \_ \_ \_ \_ Gerenciador](mf-sink-writer-d3d-manager.md) de D3D de [ \_ leitor de origem \_ \_ \_ MF](mf-source-reader-d3d-manager.md) ou do gravador de coletor MF.

Se o aplicativo habilitar o suporte a Direct3D, o leitor de origem e o gravador de coletor tentarão alocar superfícies de Direct3D para vídeo. Se isso falhar e o \_ \_ atributo opcional MF ReadWrite D3D \_ for **true**, o gravador de leitor/coletor de origem retornará para alocar superfícies de vídeo na memória do sistema. Caso contrário, se as superfícies do Direct3D não puderem ser alocadas e \_ o MF ReadWrite \_ D3D \_ opcional for **false**, ocorrerá um erro durante o processamento.

Se o aplicativo não habilitar o suporte a Direct3D, o gravador leitor/coletor de origem usará a memória do sistema e ignorará o valor do MF \_ ReadWrite \_ D3D \_ opcional.

Esse atributo é opcional. O valor padrão é **FALSE**. Defina o atributo ao criar o leitor de origem ou o gravador de coletor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do gravador de coletor](sink-writer-attributes.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




