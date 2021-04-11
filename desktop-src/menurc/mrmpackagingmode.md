---
title: Enumeração MrmPackagingMode (MrmResourceIndexer. h)
description: Define constantes que especificam que tipo de arquivo PRI deve ser criado por MrmCreateResourceFile e MrmCreateResourceFileInMemory.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Menus de enumeração MrmPackagingMode e outros recursos
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295796"
---
# <a name="mrmpackagingmode-enumeration"></a>Enumeração MrmPackagingMode

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Define constantes que especificam que tipo de arquivo PRI deve ser criado por [**MrmCreateResourceFile**](mrmcreateresourcefile.md) e [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md). Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**
</dt> <dd>

Especifica que um único arquivo PRI deve ser criado.

</dd> <dt>

<span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**
</dt> <dd>

Especifica que vários arquivos PRI devem ser criados; dividir automaticamente por todos os qualificadores com suporte (especificamente, idioma e escala).

</dd> <dt>

<span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**
</dt> <dd>

Especifica que um arquivo PRI satélite de complemento deve ser criado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

