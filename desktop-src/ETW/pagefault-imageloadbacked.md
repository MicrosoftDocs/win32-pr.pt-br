---
description: Essa classe é a classe de tipo de evento para carregamento de imagem em eventos de arquivo de paginação. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: Classe PageFault_ImageLoadBacked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968034"
---
# <a name="pagefault_imageloadbacked-class"></a>\_Classe falhadepágina ImageLoadBacked

Essa classe é a classe de tipo de evento para carregamento de imagem em eventos de arquivo de paginação.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a>Membros

A classe **falhadepágina \_ ImageLoadBacked** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **falhadepágina \_ ImageLoadBacked** tem essas propriedades.

<dl> <dt>

**DeviceChar**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), formato ("x")
</dt> </dl>

Reservado.

</dd> <dt>

**Filechar**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3), formato ("x")
</dt> </dl>

Reservado.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**de \_ nome de FileIo**](fileio-name.md) para determinar o nome do arquivo.

</dd> <dt>

**Sinalizadores de**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4), formato ("x")
</dt> </dl>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O evento é registrado durante uma criação de seção de imagem (por exemplo, uma carga de DLL) quando o Gerenciador de memória determina que a imagem precisa ser copiada e executada a partir do arquivo de paginação. Normalmente, as imagens são executadas a partir do arquivo de origem, mas o backup de paginação pode ocorrer quando o Gerenciador de memória determina que o arquivo de origem pode ser modificado de forma assíncrona por gravadores existentes ou quando o arquivo de origem está em uma mídia removível ou em um dispositivo remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Falhadepágina \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




