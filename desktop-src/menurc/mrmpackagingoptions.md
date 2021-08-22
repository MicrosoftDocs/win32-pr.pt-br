---
title: Enumeração MrmPackagingOptions (MrmResourceIndexer. h)
description: Define constantes que especificam opções para o arquivo PRI criado por MrmCreateResourceFile e MrmCreateResourceFileInMemory.
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- Menus de enumeração MrmPackagingOptions e outros recursos
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede8ef1367bc217827f616514a4fb9ea69e180cb654a19cbbe9593d4c74036d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971965"
---
# <a name="mrmpackagingoptions-enumeration"></a>Enumeração MrmPackagingOptions

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Define constantes que especificam opções para o arquivo PRI criado por [**MrmCreateResourceFile**](mrmcreateresourcefile.md) e [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md). Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**
</dt> <dd>

Especifica nenhuma opção de empacotamento.

</dd> <dt>

<span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**
</dt> <dd>

Especifica que um pacote de recursos sem esquema deve ser criado.

</dd> <dt>

<span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**
</dt> <dd>

Especifica que o arquivo PRI deve ser dividido automaticamente por todos os qualificadores com suporte (especificamente, idioma e escala).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1803\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

