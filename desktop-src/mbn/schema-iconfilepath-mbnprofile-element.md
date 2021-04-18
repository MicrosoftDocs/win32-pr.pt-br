---
description: Contém o caminho do arquivo de ícone para a conexão.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Elemento ICONFilePath (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808245"
---
# <a name="iconfilepath-mbnprofile-element"></a>Elemento ICONFilePath (MBNProfile)

O elemento **ICONFilePath (MBNProfile)** contém o caminho do arquivo de ícone para a conexão.

A interface do usuário da conexão do sistema operacional exibirá esse ícone quando uma conexão for feita usando esse elemento.

Ao passar o XML para criar o perfil no método [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) da interface [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) , esse caminho deve apontar para o local de origem do arquivo de ícone. Após a criação bem-sucedida do objeto [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) , o serviço de banda larga móvel copiará o arquivo de ícone no repositório interno e o caminho do perfil será modificado para refletir isso.

O arquivo de ícone deve estar no formato. bmp com a dimensão de 32X32 x 32 pixels.

Esse elemento é uma cadeia de caracteres com comprimento de até 1024 caracteres, contendo um caminho de arquivo absoluto.

O elemento é opcional.

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

O elemento **ICONFilePath** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




