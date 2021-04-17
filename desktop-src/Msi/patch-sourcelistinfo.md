---
description: A propriedade SourceListInfo do objeto patch Obtém e define as propriedades de informações de origem para um patch. Esta propriedade chama MsiSourceListGetInfo ou MsiSourceListSetInfo. Esta é uma propriedade de leitura ou gravação.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Propriedade patch. SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747747"
---
# <a name="patchsourcelistinfo-property"></a>Propriedade patch. SourceListInfo

A propriedade **SourceListInfo** do objeto [**patch**](patch-object.md) Obtém e define as propriedades de informações de origem para um patch. Esta propriedade chama [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) ou [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa). Esta é uma propriedade de leitura ou gravação.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a>Valor da propriedade

O nome das propriedades de informações de origem para um patch a ser consultado ou definido. Para obter os valores possíveis, consulte a seção comentários deste tópico.

## <a name="remarks"></a>Comentários

Nem todas as propriedades que podem ser recuperadas podem ser definidas. O parâmetro *szProperty* pode ser um dos valores a seguir.



| Propriedade         | Pode definir? | Significado                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | S        | O caminho relativo à raiz da mídia de instalação.                                                                                                                                                                                                          |
| DiskPrompt       | S        | O modelo de prompt usado ao solicitar a mídia de instalação do usuário.                                                                                                                                                                                          |
| LastUsedSource   | S        | O local de origem usado mais recentemente para o patch. Quando você define essa propriedade, Prefixe o local de origem com "n;" para uma fonte de rede ou "u;" para o tipo de URL. Por exemplo, use "n; \\ \\ \\ \\ teste de rascunho transitório "ou" u; https://microsoft.com/Patches/Office/SP1 ". |
| LastUsedType     | N        | "n" se a fonte do último usado for um local de rede. "u" se a última origem usada era um local de URL. "m" se a última origem usada era a mídia. Cadeia de caracteres vazia ("") se não houver uma última fonte usada.                                                                      |
| PackageName      | S        | O nome do pacote de Windows Installer ou pacote de patch na origem.                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




