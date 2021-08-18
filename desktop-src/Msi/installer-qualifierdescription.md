---
description: A propriedade QualifierDescription somente leitura retorna uma cadeia de caracteres de texto que descreve o componente qualificado.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Propriedade Installer.QualifierDescription
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c226f00d7f95b4585fa4a0713fb281011079cdc35c4e421254beec75db84d7db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763576"
---
# <a name="installerqualifierdescription-property"></a>Propriedade Installer.QualifierDescription

A propriedade **QualifierDescription** somente leitura retorna uma cadeia de caracteres de texto que descreve o componente qualificado. Essa cadeia de caracteres localizável é publicada na coluna AppData da tabela [PublishComponent](publishcomponent-table.md) e pode ser exibida ao usuário. O qualificador distingue várias formas do mesmo componente, como um componente implementado em vários idiomas.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Componentes qualificados](qualified-components.md)
</dt> </dl>

 

 




