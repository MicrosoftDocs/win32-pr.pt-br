---
description: Especifica se o aplicativo requer suporte ao Microsoft Direct3D no leitor de origem ou no gravador de coletor.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: Atributo MF_READWRITE_D3D_OPTIONAL (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171727"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>\_ \_ Atributo opcional MF ReadWrite D3D \_

Especifica se o aplicativo requer suporte ao Microsoft Direct3D no [leitor de origem](source-reader.md) ou no [gravador de coletor](sink-writer.md).

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplicará somente se o aplicativo habilitar o suporte a Direct3D usando o atributo de [ \_ \_ \_ \_ Gerenciador](mf-sink-writer-d3d-manager.md) de D3D de [ \_ leitor de origem \_ \_ \_ MF](mf-source-reader-d3d-manager.md) ou do gravador de coletor MF.

Se o aplicativo habilitar o suporte a Direct3D, o leitor de origem e o gravador de coletor tentarão alocar superfícies de Direct3D para vídeo. Se isso falhar e o \_ \_ atributo opcional MF ReadWrite D3D \_ for **true**, o gravador de leitor/coletor de origem retornará para alocar superfícies de vídeo na memória do sistema. Caso contrário, se as superfícies do Direct3D não puderem ser alocadas e \_ o MF ReadWrite \_ D3D \_ opcional for **false**, ocorrerá um erro durante o processamento.

Se o aplicativo não habilitar o suporte a Direct3D, o gravador leitor/coletor de origem usará a memória do sistema e ignorará o valor do MF \_ ReadWrite \_ D3D \_ opcional.

Esse atributo é opcional. O valor padrão é **false**. Defina o atributo ao criar o leitor de origem ou o gravador de coletor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do gravador de coletor](sink-writer-attributes.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




