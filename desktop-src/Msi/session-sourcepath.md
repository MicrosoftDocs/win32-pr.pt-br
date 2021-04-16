---
description: A Propriedade SourcePath do objeto de sessão é uma propriedade somente leitura que fornece o caminho completo para a pasta designada na imagem de mídia ou do servidor de origem.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Propriedade Session. SourcePath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757785"
---
# <a name="sessionsourcepath-property"></a>Propriedade Session. SourcePath

A propriedade **SourcePath** do objeto de [**sessão**](session-object.md) é uma propriedade somente leitura que fornece o caminho completo para a pasta designada na imagem de mídia ou do servidor de origem.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a>Valor da propriedade

Nome necessário diferenciar maiúsculas de minúsculas de uma propriedade de pasta, conforme especificado por uma chave primária da [tabela de diretórios](directory-table.md). Um erro será gerado se a pasta não existir.

## <a name="remarks"></a>Comentários

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




