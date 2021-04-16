---
description: A propriedade QualifierDescription somente leitura retorna uma cadeia de texto que descreve o componente qualificado.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Propriedade Installer. QualifierDescription
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
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752250"
---
# <a name="installerqualifierdescription-property"></a>Propriedade Installer. QualifierDescription

A propriedade **QualifierDescription** somente leitura retorna uma cadeia de texto que descreve o componente qualificado. Essa cadeia de caracteres localizável é criada na coluna AppData da [tabela PublishComponent](publishcomponent-table.md) e pode ser exibida para o usuário. O qualificador distingue várias formas do mesmo componente, como um componente que é implementado em vários idiomas.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Componentes qualificados](qualified-components.md)
</dt> </dl>

 

 




