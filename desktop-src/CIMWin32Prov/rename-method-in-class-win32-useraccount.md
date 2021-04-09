---
description: Renomeia um nome de conta de usuário.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Método Rename da classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089478"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a>Método Rename da \_ classe USERACCOUNT do Win32

O método **renomear** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomeia um nome de conta de usuário.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ do no\]
</dt> <dd>

Nome da nova conta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Êxito**
</dt> <dd>

0

Sucesso.

</dd> <dt>

**Instância não encontrada**
</dt> <dd>

1

Instância não encontrada.

</dd> <dt>

**Instância necessária**
</dt> <dd>

2

Instância necessária.

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

3

Parâmetro inválido.

</dd> <dt>

**Usuário não encontrado**
</dt> <dd>

4

Usuário não encontrado.

</dd> <dt>

**Domínio não encontrado**
</dt> <dd>

5

Domínio não encontrado.

</dd> <dt>

**A operação é permitida somente no controlador de domínio primário do domínio**
</dt> <dd>

6

A operação é permitida somente no controlador de domínio primário do domínio.

</dd> <dt>

**A operação não é permitida na última conta administrativa.**
</dt> <dd>

7

</dd> <dt>

**A operação não é permitida em grupos especiais especificados; usuário, administrador, local ou convidado.**
</dt> <dd>

8

A operação não é permitida em grupos especiais especificados: usuário, administrador, local ou convidado.

</dd> <dt>

**Outro erro de API**
</dt> <dd>

9

Outro erro de API.

</dd> <dt>

**Erro interno**
</dt> <dd>

10

Erro interno.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa funcionalidade é implementada como um método para fornecer um contexto separado para o novo nome que é distinguivel do valor da propriedade de chave para o nome que está associado à instância a ser modificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Conta userwin32 \_**](win32-useraccount.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

