---
description: A propriedade SourceListInfo do objeto Patch obtém e define as propriedades de informações de origem para um patch. Essa propriedade chama MsiSourceListGetInfo ou MsiSourceListSetInfo. Essa é uma propriedade de leitura ou gravação.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Propriedade Patch.SourceListInfo
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
ms.openlocfilehash: 9832fbe811f012932e4fb96bb8f530c4fc49d614ed5960c9f94065388f373833
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534436"
---
# <a name="patchsourcelistinfo-property"></a>Propriedade Patch.SourceListInfo

A **propriedade SourceListInfo** do objeto [**Patch**](patch-object.md) obtém e define as propriedades de informações de origem para um patch. Essa propriedade chama [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) ou [**MsiSourceListSetInfo.**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) Essa é uma propriedade de leitura ou gravação.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a>Valor da propriedade

O nome das propriedades de informações de origem de um patch a ser consultado ou definido. Para ver os valores possíveis, consulte a seção Comentários deste tópico.

## <a name="remarks"></a>Comentários

Nem todas as propriedades que podem ser recuperadas podem ser definidas. O *parâmetro szProperty* pode ser um dos valores a seguir.



| Propriedade         | Pode definir? | Significado                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | Y        | O caminho relativo à raiz da mídia de instalação.                                                                                                                                                                                                          |
| DiskPrompt       | Y        | O modelo de prompt usado ao solicitar ao usuário a mídia de instalação.                                                                                                                                                                                          |
| LastUsedSource   | Y        | O local de origem usado mais recentemente para o patch. Ao definir essa propriedade, prefixe o local de origem com "n;" para uma fonte de rede ou "u;" para o tipo de URL. Por exemplo, use "n; \\ \\ teste \\ de \\ rascunho" ou "u; https://microsoft.com/Patches/Office/SP1 ". |
| LastUsedType     | N        | "n" se a origem usada pela última vez for um local de rede. "u" se a última fonte usada foi um local de URL. "m" se a última fonte usada for mídia. Cadeia de caracteres vazia ("") se não houver nenhuma fonte usada pela última vez.                                                                      |
| PackageName      | Y        | O nome do pacote Windows instalador ou pacote de patch na origem.                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 3.0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch é definido como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




