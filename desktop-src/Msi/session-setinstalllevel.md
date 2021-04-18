---
description: O método SetInstallLevel do objeto Session define o nível de instalação para a instalação atual com um valor especificado e recalcula os Estados Select e installed para todos os recursos na tabela de recursos.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Método Session. SetInstallLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751628"
---
# <a name="sessionsetinstalllevel-method"></a>Método Session. SetInstallLevel

O método **SetInstallLevel** do objeto [**Session**](session-object.md) define o nível de instalação para a instalação atual com um valor especificado e recalcula os Estados Select e installed para todos os recursos na tabela de recursos. Ele também define o estado de ação de cada componente na [tabela de componentes](component-table.md) com base no novo nível.

## <a name="syntax"></a>Sintaxe


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*installLevel* 
</dt> <dd>

Novo nível de instalação solicitado necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A [ação CostInitialize](costinitialize-action.md) deve ser executada antes de chamar **SetInstallLevel**.

Se 0 for passado para o parâmetro *installLevel* , o nível de instalação atual não será alterado, mas todos os recursos ainda serão atualizados com base no nível de instalação atual. Por exemplo, essa funcionalidade pode ser usada pelo módulo manipulador para redefinir todas as seleções de volta para seus Estados padrão iniciais em qualquer ponto do processo de seleção de interface do usuário.

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




