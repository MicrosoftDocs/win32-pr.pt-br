---
description: Especifica uma lista de comandos de script e os parâmetros para um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de comando de script no cabeçalho ASF, definido na especificação ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: Atributo MF_PD_ASF_SCRIPT (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798271"
---
# <a name="mf_pd_asf_script-attribute"></a>\_Atributo de script MF PD \_ ASF \_

Especifica uma lista de comandos de script e os parâmetros para um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de comando de script no cabeçalho ASF, definido na especificação ASF.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo a partir do cabeçalho de objeto de comando de script. A tabela a seguir mostra o formato do blob:



| Campo de objeto de comando de script | Tipo de dados    | Tamanho    | Descrição               |
|-----------------------------|--------------|---------|---------------------------|
| Contagem de comandos              | **DWORD**    | 4 bytes | Número de comandos de script |
| Tipo de comando, comandos      | **MINUCIOSA**\[\] | Varia  | Matriz de comandos de script  |



 

O primeiro **DWORD** é o número de comandos de script, seguidos por uma matriz de comandos. Cada comando de script tem o seguinte formato:



| Campo de objeto de comando de script | Tipo de dados     | Tamanho    | Descrição                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| Comprimento do nome do comando         | **DWORD**     | 4 bytes | Tamanho da cadeia de caracteres do comando, em bytes, incluindo o caractere nulo.      |
| Nome do comando                | **WCHAR**\[\] | Varia  | Cadeia de caracteres terminada em nulo que contém o comando de script.                 |
| Comprimento do nome do tipo de comando    | **DWORD**     | 4 bytes | Tamanho da cadeia de caracteres do tipo de comando, em bytes, incluindo o caractere nulo. |
| Nome do tipo de comando           | **WCHAR**\[\] | Varia  | Cadeia de caracteres terminada em nulo que contém o tipo de comando.                   |
| Tempo da apresentação           | **DWORD**     | 4 bytes | Hora da apresentação do comando em milissegundos.                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




