---
description: A propriedade ComponentClients somente leitura retorna um objeto StringList que enumera o conjunto de clientes de um componente especificado.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Propriedade Installer. ComponentClients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748983"
---
# <a name="installercomponentclients-property"></a>Propriedade Installer. ComponentClients

A propriedade **ComponentClients** somente leitura retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de clientes de um componente especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Valor da propriedade

Um GUID de cadeia de caracteres que representa o código do componente. Os códigos de componente são especificados na coluna ComponentID da [tabela de componentes](component-table.md).

## <a name="remarks"></a>Comentários

Para enumerar os clientes do componente, um aplicativo pode iterar por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each. Como os clientes não são ordenados, todos os componentes novos têm um índice arbitrário. Isso significa que a função pode retornar clientes em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




