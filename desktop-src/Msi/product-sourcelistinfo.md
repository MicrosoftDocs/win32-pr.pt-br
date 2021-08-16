---
description: A propriedade SourceListInfo do objeto Product obtém e define as propriedades de informações de origem de um produto. Essa propriedade chama MsiSourceListGetInfo ou MsiSourceListSetInfo. Essa é uma propriedade de leitura ou gravação.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Propriedade Product.SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d58bc3f9eae1f953d67d2bd83b951bda1d2fe17f3f2b00cbaa9b5b7f9ad3a968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376699"
---
# <a name="productsourcelistinfo-property"></a>Propriedade Product.SourceListInfo

A **propriedade SourceListInfo** do objeto [**Product**](product-object.md) obtém e define as propriedades de informações de origem de um produto. Essa propriedade chama [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) ou [**MsiSourceListSetInfo.**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) Essa é uma propriedade de leitura ou gravação.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a>Valor da propriedade

O nome das propriedades de informações de origem de um produto a ser consultado ou definido. Para ver os valores possíveis, consulte a seção Comentários deste tópico.

## <a name="remarks"></a>Comentários

Nem todas as propriedades que podem ser recuperadas podem ser definidas. O *parâmetro szProperty* pode ser um dos valores a seguir.



| Propriedade         | Pode definir? | Significado                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | Y        | O caminho relativo à raiz da mídia de instalação.                                                                                                                                                                                                       |
| DiskPrompt       | Y        | O modelo de prompt usado ao solicitar ao usuário a mídia de instalação.                                                                                                                                                                                       |
| LastUsedSource   | Y        | O local de origem usado mais recentemente para o produto. Ao definir essa propriedade, prefixe o local de origem com "n;" para uma fonte de rede ou "u;" para o tipo de URL. Por exemplo, "n; \\ \\ rascunho \\ \\ MySource" e "u; https://MyServer/MyFolder/MySource ". |
| LastUsedType     | N        | "n" se a origem usada pela última vez for um local de rede. "u" se a última fonte usada foi um local de URL. "m" se a última fonte usada for mídia. Cadeia de caracteres vazia ("") se não houver nenhuma fonte usada pela última vez.                                                                   |
| PackageName      | Y        | O nome do pacote Windows instalador ou pacote de patch na origem.                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 3.0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct é definido como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Produto**](product-object.md)
</dt> <dt>

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




