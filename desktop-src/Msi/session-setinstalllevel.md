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
ms.openlocfilehash: ac075bcb61cb2eedded3b6d86f3dc821c387b3dca98e9325a0fdf1b016fb31d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628806"
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

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A [ação CostInitialize](costinitialize-action.md) deve ser executada antes de chamar **SetInstallLevel**.

Se 0 for passado para o parâmetro *installLevel* , o nível de instalação atual não será alterado, mas todos os recursos ainda serão atualizados com base no nível de instalação atual. Por exemplo, essa funcionalidade pode ser usada pelo módulo manipulador para redefinir todas as seleções de volta para seus Estados padrão iniciais em qualquer ponto do processo de seleção de interface do usuário.

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




