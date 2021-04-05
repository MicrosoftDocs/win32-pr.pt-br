---
title: Métodos de propriedade IADsDomain (IADs. h)
description: Os métodos de interface IADsDomain lêem e gravam as propriedades descritas neste tópico. Para obter mais informações, consulte interface Property Methods.
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsDomain
topic_type:
- apiref
api_name:
- IADsDomain Property Methods
- IADsDomain.AutoUnlockInterval
- IADsDomain.get_AutoUnlockInterval
- IADsDomain.put_AutoUnlockInterval
- IADsDomain.IsWorkgroup
- IADsDomain.get_IsWorkgroup
- IADsDomain.LockoutObservationInterval
- IADsDomain.get_LockoutObservationInterval
- IADsDomain.put_LockoutObservationInterval
- IADsDomain.MinPasswordAge
- IADsDomain.get_MinPasswordAge
- IADsDomain.put_MinPasswordAge
- IADsDomain.MinPasswordLength
- IADsDomain.get_MinPasswordLength
- IADsDomain.put_MinPasswordLength
- IADsDomain.MaxBadPasswordsAllowed
- IADsDomain.get_MaxBadPasswordsAllowed
- IADsDomain.put_MaxBadPasswordsAllowed
- IADsDomain.MaxPasswordAge
- IADsDomain.get_MaxPasswordAge
- IADsDomain.put_MaxPasswordAge
- IADsDomain.PasswordAttributes
- IADsDomain.get_PasswordAttributes
- IADsDomain.put_PasswordAttributes
- IADsDomain.PasswordHistoryLength
- IADsDomain.get_PasswordHistoryLength
- IADsDomain.put_PasswordHistoryLength
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a10c6377c7e97f83046f60d46312a03db68cadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918893"
---
# <a name="iadsdomain-property-methods"></a>Métodos de propriedade IADsDomain

Os métodos de interface [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) lêem e gravam as propriedades descritas neste tópico. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**AutoUnlockInterval**
</dt> <dd> <dl>

Indica o tempo mínimo que deve decorrer antes que a conta seja reabilitada automaticamente.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AutoUnlockInterval(
  [out] LONG* plAutoUnlockInterval
);
HRESULT put_AutoUnlockInterval(
  [in] LONG lAutoUnlockInterval
);
```


</dt> </dl> </dd> <dt>

**Grupo de trabalho**
</dt> <dd> <dl>

Esta propriedade não é mais implementada.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados Scripting: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

**LockoutObservationInterval**
</dt> <dd> <dl>

Indica a janela de tempo durante a qual a contagem de senha inadequada é monitorada e acumulada antes de determinar se a conta precisa ser bloqueada. Por exemplo, se o número de tentativas de senha incorretas em uma conta exceder o limite (máximo de senhas incorretas permitidas) durante o período de tempo especificado (intervalo de observação de bloqueio), a conta será bloqueada definindo a propriedade apropriada no conjunto de propriedades de parâmetro de logon.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockoutObservationInterval(
  [out] LONG* plLockoutObservationInterval
);
HRESULT put_LockoutObservationInterval(
  [in] LONG lLockoutObservationInterval
);
```


</dt> </dl> </dd> <dt>

**MaxBadPasswordsAllowed**
</dt> <dd> <dl>

Indica o número máximo de logons de senha inválidos permitidos antes de um bloqueio de conta.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxBadPasswordsAllowed(
  [out] LONG* plMaxBadPasswordsAllowed
);
HRESULT put_MaxBadPasswordsAllowed(
  [in] LONG lMaxBadPasswordsAllowed
);
```


</dt> </dl> </dd> <dt>

**MaxPasswordAge**
</dt> <dd> <dl>

Indica o intervalo de tempo máximo, em segundos, após o qual a senha deve ser alterada pelo usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxPasswordAge(
  [out] LONG* plMaxPasswordAge
);
RESULT put_MaxPasswordAge(
  [in] LONG lMaxPasswordAge
);
```


</dt> </dl> </dd> <dt>

**MinPasswordAge**
</dt> <dd> <dl>

Indica o intervalo de tempo mínimo, em segundos, antes que a senha possa ser alterada.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordAge(
  [out] LONG* plMinPasswordAge
);
HRESULT put_MinPasswordAge(
  [in] LONG lMinPasswordAge
);
```


</dt> </dl> </dd> <dt>

**MinPasswordLength**
</dt> <dd> <dl>

Indica o número mínimo de caracteres que devem ser usados para uma senha.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordLength(
  [out] LONG* plMinPasswordLength
);
HRESULT put_MinPasswordLength(
  [in] LONG lMinPasswordLength
);
```


</dt> </dl> </dd> <dt>

**Senhaattributes**
</dt> <dd> <dl>

Indica restrições em senhas, conforme definido pela lista de atributos e valores a seguir.

> [!Note]  
> Para \_ a atributo de senha \_ complexo, a senha deve incluir pelo menos uma marca de pontuação ou um caractere não imprimível.

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

**Senha \_ do ATTR \_ None** (0x00000000)


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

**Senha \_ do \_ \_ Diferenciar maiúsculas de minúsculas** (0x00000001)


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

**Senha \_ do ATTR \_ complexo** (0x00000002)


</dt> <dd></dd> </dl> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordAttributes(
  [out] LONG* plPasswordAttributes
);
HRESULT put_PasswordAttributes(
  [in] LONG lPasswordAttributes
);
```


</dt> </dl> </dd> <dt>

**PasswordHistoryLength**
</dt> <dd> <dl>

Indica o número de senhas anteriores salvas na lista de histórico. O usuário não pode reutilizar uma senha na lista de histórico.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordHistoryLength(
  [out] LONG* plPasswordHistoryLength
);
HRESULT put_PasswordHistoryLength(
  [in] LONG lPasswordHistoryLength
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir exibe o valor da propriedade **PasswordHistoryLength** .


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



O exemplo de código a seguir exibe o valor da propriedade **PasswordHistoryLength** .


```C++
LPWSTR adsPath = L"WinNT://myDomain";
LONG nPasswordHistoryLength = 0;

// Bind to the domain object.
hr = ADsGetObject(adsPath,IID_IADsDomain,(void**)&pDomain);
if(FAILED(hr)) {goto Cleanup;}

hr = pDomain->get_PasswordHistoryLength(&nPasswordHistoryLength);
if(FAILED(hr)) {goto Cleanup;}
printf("Password history length: %d",nPasswordHistoryLength);

Cleanup:
    if(pDomain) pDomain->Release();
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsDomain é definido como 00E4C220-FD16-11CE-ABC4-02608C9E7553<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[Métodos de propriedade de interface](interface-property-methods.md)
</dt> </dl>

 

 





