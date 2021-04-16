---
description: A propriedade TargetPath do objeto de sessão é uma propriedade de leitura/gravação que fornece o caminho completo para a pasta designada na unidade de destino da instalação.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Propriedade Session. TargetPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750216"
---
# <a name="sessiontargetpath-property"></a>Propriedade Session. TargetPath

A propriedade **TargetPath** do objeto de [**sessão**](session-object.md) é uma propriedade de leitura/gravação que fornece o caminho completo para a pasta designada na unidade de destino da instalação.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a>Valor da propriedade

Nome necessário diferenciar maiúsculas de minúsculas de uma propriedade de pasta, conforme especificado por uma chave primária da [tabela de diretórios](directory-table.md). Um erro será gerado se a pasta não existir.

## <a name="remarks"></a>Comentários

Não tente configurar o caminho de destino se os componentes que usam esses caminhos já estiverem instalados para o usuário atual ou para um usuário diferente. Verifique a propriedade [**productstate**](productstate.md) para determinar se o produto que contém o componente está instalado.

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




