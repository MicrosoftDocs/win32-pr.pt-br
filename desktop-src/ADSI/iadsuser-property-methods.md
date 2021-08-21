---
title: Métodos de propriedade IADsUser (IADs. h)
description: Os métodos de propriedade da interface IADsUser obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 02d0e5f1-8bc9-4ef6-962d-432654ca8433
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsUser
topic_type:
- apiref
api_name:
- IADsUser Property Methods
- IADsUser.AccountDisabled
- IADsUser.get_AccountDisabled
- IADsUser.put_AccountDisabled
- IADsUser.AccountExpirationDate
- IADsUser.get_AccountExpirationDate
- IADsUser.put_AccountExpirationDate
- IADsUser.BadLoginAddress
- IADsUser.get_BadLoginAddress
- IADsUser.BadLoginCount
- IADsUser.get_BadLoginCount
- IADsUser.Department
- IADsUser.get_Department
- IADsUser.put_Department
- IADsUser.Description
- IADsUser.get_Description
- IADsUser.put_Description
- IADsUser.Division
- IADsUser.get_Division
- IADsUser.put_Division
- IADsUser.EmailAddress
- IADsUser.get_EmailAddress
- IADsUser.put_EmailAddress
- IADsUser.EmployeeID
- IADsUser.get_EmployeeID
- IADsUser.put_EmployeeID
- IADsUser.FaxNumber
- IADsUser.get_FaxNumber
- IADsUser.put_FaxNumber
- IADsUser.FirstName
- IADsUser.get_FirstName
- IADsUser.put_FirstName
- IADsUser.FullName
- IADsUser.get_FullName
- IADsUser.put_FullName
- IADsUser.GraceLoginsAllowed
- IADsUser.get_GraceLoginsAllowed
- IADsUser.put_GraceLoginsAllowed
- IADsUser.GraceLoginsRemaining
- IADsUser.get_GraceLoginsRemaining
- IADsUser.put_GraceLoginsRemaining
- IADsUser.HomeDirectory
- IADsUser.get_HomeDirectory
- IADsUser.put_HomeDirectory
- IADsUser.HomePage
- IADsUser.get_HomePage
- IADsUser.put_HomePage
- IADsUser.IsAccountLocked
- IADsUser.get_IsAccountLocked
- IADsUser.put_IsAccountLocked
- IADsUser.Languages
- IADsUser.get_Languages
- IADsUser.put_Languages
- IADsUser.LastFailedLogin
- IADsUser.get_LastFailedLogin
- IADsUser.LastLogin
- IADsUser.get_LastLogin
- IADsUser.LastLogoff
- IADsUser.get_LastLogoff
- IADsUser.LastName
- IADsUser.get_LastName
- IADsUser.put_LastName
- IADsUser.LoginHours
- IADsUser.get_LoginHours
- IADsUser.put_LoginHours
- IADsUser.LoginScript
- IADsUser.get_LoginScript
- IADsUser.put_LoginScript
- IADsUser.LoginWorkstations
- IADsUser.get_LoginWorkstations
- IADsUser.put_LoginWorkstations
- IADsUser.Manager
- IADsUser.get_Manager
- IADsUser.put_Manager
- IADsUser.MaxLogins
- IADsUser.get_MaxLogins
- IADsUser.put_MaxLogins
- IADsUser.MaxStorage
- IADsUser.get_MaxStorage
- IADsUser.put_MaxStorage
- IADsUser.NamePrefix
- IADsUser.get_NamePrefix
- IADsUser.put_NamePrefix
- IADsUser.NameSuffix
- IADsUser.get_NameSuffix
- IADsUser.put_NameSuffix
- IADsUser.OfficeLocations
- IADsUser.get_OfficeLocations
- IADsUser.put_OfficeLocations
- IADsUser.OtherName
- IADsUser.get_OtherName
- IADsUser.put_OtherName
- IADsUser.PasswordExpirationDate
- IADsUser.get_PasswordExpirationDate
- IADsUser.put_PasswordExpirationDate
- IADsUser.PasswordLastChanged
- IADsUser.get_PasswordLastChanged
- IADsUser.PasswordMinimumLength
- IADsUser.get_PasswordMinimumLength
- IADsUser.put_PasswordMinimumLength
- IADsUser.PasswordRequired
- IADsUser.get_PasswordRequired
- IADsUser.put_PasswordRequired
- IADsUser.Picture
- IADsUser.get_Picture
- IADsUser.put_Picture
- IADsUser.PostalAddresses
- IADsUser.get_PostalAddresses
- IADsUser.put_PostalAddresses
- IADsUser.PostalCodes
- IADsUser.get_PostalCodes
- IADsUser.put_PostalCodes
- IADsUser.Profile
- IADsUser.get_Profile
- IADsUser.put_Profile
- IADsUser.RequireUniquePassword
- IADsUser.get_RequireUniquePassword
- IADsUser.put_RequireUniquePassword
- IADsUser.SeeAlso
- IADsUser.get_SeeAlso
- IADsUser.put_SeeAlso
- IADsUser.TelephoneHome
- IADsUser.get_TelephoneHome
- IADsUser.put_TelephoneHome
- IADsUser.TelephoneMobile
- IADsUser.get_TelephoneMobile
- IADsUser.put_TelephoneMobile
- IADsUser.TelephoneNumber
- IADsUser.get_TelephoneNumber
- IADsUser.put_TelephoneNumber
- IADsUser.TelephonePager
- IADsUser.get_TelephonePager
- IADsUser.put_TelephonePager
- IADsUser.Title
- IADsUser.get_Title
- IADsUser.put_Title
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd41380e2c8ca58f5ce530f4c3024eb43522b474f128c3a296aaf5b4d84937f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082370"
---
# <a name="iadsuser-property-methods"></a>Métodos de propriedade IADsUser

Os métodos de propriedade da interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**AccountDisabled**
</dt> <dd> <dl>

Um sinalizador para indicar se a conta é ou deve ser desativada.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **booliano**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccountDisabled(
  [out] VARIANT_BOOL* pfAccountDisabled
);
HRESULT put_AccountDisabled(
  [in] VARIANT_BOOL fAccountDisabled
);
```


</dt> </dl> </dd> <dt>

**AccountExpirationDate**
</dt> <dd> <dl>

A data e a hora após as quais o usuário não pode fazer logon.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Data**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccountExpirationDate(
  [out] DATE* pdateAccountExpirationDate
);
HRESULT put_AccountExpirationDate(
  [in] DATE dateAccountExpirationDate
);
```


</dt> </dl> </dd> <dt>

**BadLoginAddress**
</dt> <dd> <dl>

O último nó que é considerado um intruso possível; Isso estará disponível se a detecção de intrusos estiver ativa.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BadLoginAddress(
  [out] BSTR* pbstrBadLoginAddress
);
```


</dt> </dl> </dd> <dt>

**BadLoginCount**
</dt> <dd> <dl>

O número de tentativas de logon inválidos desde a última redefinição.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BadLoginCount(
  [out] LONG* plBadLoginCount
);
```


</dt> </dl> </dd> <dt>

**Departamento**
</dt> <dd> <dl>

O departamento, uma UO (unidade organizacional), dentro da empresa à qual o usuário pertence.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

**Descrição**
</dt> <dd> <dl>

A descrição do texto do usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

**Divisão**
</dt> <dd> <dl>

A divisão em uma empresa ou organização.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

**EmailAddress**
</dt> <dd> <dl>

O endereço de email do usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EmailAddress(
  [out] BSTR* pbstrEmailAddress
);
HRESULT put_EmailAddress(
  [in] BSTR bstrEmailAddress
);
```


</dt> </dl> </dd> <dt>

**EmployeeID**
</dt> <dd> <dl>

O identificador de funcionário do usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EmployeeID(
  [out] BSTR* pbstrEmployeeID
);
HRESULT put_EmployeeID(
  [in] BSTR bstrEmployeeID
);
```


</dt> </dl> </dd> <dt>

**FaxNumber**
</dt> <dd> <dl>

O número de fax, ou números, do usuário. Em Active Directory, essa propriedade é de valor único e a matriz **Variant** tem um elemento.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] VARIANT* pvarFaxNumber
);
HRESULT put_FaxNumber(
  [in] VARIANT varFaxNumber
);
```


</dt> </dl> </dd> <dt>

**Nome**
</dt> <dd> <dl>

Primeiro nome do usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FirstName(
  [out] BSTR* pbstrFirstName
);
HRESULT put_FirstName(
  [in] BSTR bstrFirstName
);
```


</dt> </dl> </dd> <dt>

**FullName**
</dt> <dd> <dl>

O nome completo do usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FullName(
  [out] BSTR* pbstrFullName
);
HRESULT put_FullName(
  [in] BSTR bstrFullName
);
```


</dt> </dl> </dd> <dt>

**GraceLoginsAllowed**
</dt> <dd> <dl>

O número de vezes que o usuário pode fazer logon depois que a senha tiver expirado.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GraceLoginsAllowed(
  [out] LONG* plGraceLoginsAllowed
);
HRESULT put_GraceLoginsAllowed(
  [in] LONG lGraceLoginsAllowed
);
```


</dt> </dl> </dd> <dt>

**GraceLoginsRemaining**
</dt> <dd> <dl>

O número de logons permitidos antes que a conta seja bloqueada.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GraceLoginsRemaining(
  [out] LONG* plGraceLoginsRemaining
);
HRESULT put_GraceLoginsRemaining(
  [in] LONG lGraceLoginsRemaining
);
```


</dt> </dl> </dd> <dt>

**HomeDirectory**
</dt> <dd> <dl>

O diretório base do usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HomeDirectory(
  [out] BSTR* pbstrHomeDirectory
);
HRESULT put_HomeDirectory(
  [in] BSTR bstrHomeDirectory
);
```


</dt> </dl> </dd> <dt>

**Principal**
</dt> <dd> <dl>

A URL para a home page do usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HomePage(
  [out] BSTR* pbstrHomePage
);
HRESULT put_HomePage(
  [in] BSTR bstrHomePage
);
```


</dt> </dl> </dd> <dt>

**IsAccountLocked**
</dt> <dd> <dl>

Um sinalizador que indica se a conta está bloqueada devido à detecção de intrusos. Essa propriedade tem uso limitado quando usada com o provedor ADSI LDAP. Para obter mais informações sobre essas limitações, consulte [bloqueio de conta (provedor LDAP)](ldap-account-lockout.md).

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **booliano**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsAccountLocked(
  [out] VARIANT_BOOL* pfIsAccountLocked
);
HRESULT put_IsAccountLocked(
  [in] VARIANT_BOOL fIsAccountLocked
);
```


</dt> </dl> </dd> <dt>

**Idiomas**
</dt> <dd> <dl>

Uma matriz de nomes de linguagem **BSTR** para o usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Languages(
  [out] VARIANT* pvLanguages
);
HRESULT put_Languages(
  [in] VARIANT vLanguages
);
```


</dt> </dl> </dd> <dt>

**LastFailedLogin**
</dt> <dd> <dl>

A data e a hora do último logon de rede com falha.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **Data**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LastFailedLogin(
  [out] DATE* pdateLastFailedLogin
);
```


</dt> </dl> </dd> <dt>

**LastLogin**
</dt> <dd> <dl>

A data e a hora do último logon de rede.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **Data**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LastLogin(
  [out] DATE* pdateLastLogin
);
```


</dt> </dl> </dd> <dt>

**LastLogoff**
</dt> <dd> <dl>

A data e a hora do último logoff de rede.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **Data**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LastLogoff(
  [out] DATE* pdateLastLogoff
);
```


</dt> </dl> </dd> <dt>

**Sobrenome**
</dt> <dd> <dl>

Sobrenome do usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LastName(
  [out] BSTR* pbstrLastName
);
HRESULT put_LastName(
  [in] BSTR bstrLastName
);
```


</dt> </dl> </dd> <dt>

**LoginHours**
</dt> <dd> <dl>

Períodos de tempo para cada dia da semana durante os quais os logons são permitidos para o usuário. Representado como uma tabela de valores booliano para a semana, cada um indicando se esse slot de tempo é uma hora de logon válida. Esteja ciente de que a representação é específica do provedor e do diretório.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoginHours(
  [out] VARIANT* pvLoginHours
);
HRESULT put_LoginHours(
  [in] VARIANT vLoginHours
);
```


</dt> </dl> </dd> <dt>

**LoginScript**
</dt> <dd> <dl>

O caminho do script de logon.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoginScript(
  [out] BSTR* pbstrLoginScript
);
HRESULT put_LoginScript(
  [in] BSTR bstrLoginScript
);
```


</dt> </dl> </dd> <dt>

**LoginWorkstations**
</dt> <dd> <dl>

Endereços ou nomes de estações de trabalho, do **tipo de dados BSTR,** do qual o usuário pode fazer logon.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoginWorkstations(
  [out] VARIANT* pvLoginWorkstations
);
HRESULT put_LoginWorkstations(
  [in] VARIANT vLoginWorkstations
);
```


</dt> </dl> </dd> <dt>

**Gerente**
</dt> <dd> <dl>

O gerente do usuário.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Manager(
  [out] BSTR* pbstrManager
);
HRESULT put_Manager(
  [in] BSTR bstrManager
);
```


</dt> </dl> </dd> <dt>

**MaxLogins**
</dt> <dd> <dl>

O número de sessões de logon simultâneas permitidas.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxLogins(
  [out] LONG* plMaxLogins
);
HRESULT put_MaxLogins(
  [in] LONG lMaxLogins
);
```


</dt> </dl> </dd> <dt>

**MaxStorage**
</dt> <dd> <dl>

A quantidade máxima de espaço em disco, em quilobytes, que o usuário pode usar.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxStorage(
  [out] LONG* plMaxStorage
);
HRESULT put_MaxStorage(
  [in] LONG lMaxStorage
);
```


</dt> </dl> </dd> <dt>

**NamePrefix**
</dt> <dd> <dl>

Prefixo de nome do usuário, por exemplo "Ms." ou "Hon".

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamePrefix(
  [out] BSTR* pbstrNamePrefix
);
HRESULT put_NamePrefix(
  [in] BSTR bstrNamePrefix
);
```


</dt> </dl> </dd> <dt>

**NameSuffix**
</dt> <dd> <dl>

Sufixo de nome do usuário, por exemplo "Jr." ou "III".

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NameSuffix(
  [out] BSTR* pbstrNameSuffix
);
HRESULT put_NameSuffix(
  [in] BSTR bstrNameSuffix
);
```


</dt> </dl> </dd> <dt>

**OfficeLocations**
</dt> <dd> <dl>

Office local como uma **matriz BSTR** para o usuário. Para o Active Directory, essa propriedade tem valor único e a matriz tem um elemento.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OfficeLocations(
  [out] VARIANT* pvOfficeLocations
);
HRESULT put_OfficeLocations(
  [in] VARIANT vOfficeLocations
);
```


</dt> </dl> </dd> <dt>

**OtherName**
</dt> <dd> <dl>

Um nome adicional, por exemplo, o nome do meio, para o usuário.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OtherName(
  [out] BSTR* pbstrOtherName
);
HRESULT put_OtherName(
  [in] BSTR bstrOtherName
);
```


</dt> </dl> </dd> <dt>

**PasswordExpirationDate**
</dt> <dd> <dl>

A data e a hora em que a senha expira.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **DATE**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordExpirationDate(
  [out] DATE* pdatePasswordExpirationDate
);
HRESULT put_PasswordExpirationDate(
  [in] DATE datePasswordExpirationDate
);
```


</dt> </dl> </dd> <dt>

**PasswordLastChanged**
</dt> <dd> <dl>

A última vez em que a senha foi alterada.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **DATE**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordLastChanged(
  [out] DATE* pdatePasswordLastChanged
);
```


</dt> </dl> </dd> <dt>

**PasswordMinimumLength**
</dt> <dd> <dl>

O comprimento mínimo da senha.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordMinimumLength(
  [out] LONG* plPasswordMinimumLength
);
HRESULT put_PasswordMinimumLength(
  [in] LONG lPasswordMinimumLength
);
```


</dt> </dl> </dd> <dt>

**PasswordRequired**
</dt> <dd> <dl>

Um sinalizador que indica se a senha é necessária.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **booliana**
</dt> <dt>



``` syntax
// C++ method syntax
VARIANT_BOOL get_PasswordRequired(
  [out] VARIANT_BOOL* pfPasswordRequired
);
HRESULT put_PasswordRequired(
  [in] VARIANT_BOOL fPasswordRequired
);
```


</dt> </dl> </dd> <dt>

**Imagem**
</dt> <dd> <dl>

Uma matriz OctetString de bytes que armazena uma imagem.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Picture(
  [out] VARIANT* pvarPicture
);
HRESULT put_Picture(
  [in] VARIANT varPicture
);
```


</dt> </dl> </dd> <dt>

**PostalAddresses**
</dt> <dd> <dl>

Endereço postal como uma **matriz BSTR.** Essa propriedade tem vários valores para conter mais de endereços do usuário. O formato interno de um PostalAddress deve estar em conformidade com CCITT F.401, conforme referenciado em X.521-1993, que define um PostalAddress como seis elementos de 30 bytes cada, mantendo um endereço de rua, (opcionalmente) Post Office Box, cidade ou localidade, estado ou província, CEP e País/Região.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddresses(
  [out] VARIANT* pvPostalAddresses
);
HRESULT put_PostalAddresses(
  [in] VARIANT vPostalAddresses
);
```


</dt> </dl> </dd> <dt>

**CepCodes**
</dt> <dd> <dl>

Códigos postais como uma **matriz BSTR.** Os códigos postais são vinculados positicamente à **matriz PostalAddresses.** No Active Directory, no entanto, essa propriedade tem valor único e a matriz tem um único elemento.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalCodes(
  [out] VARIANT* pvPostalCodes
);
HRESULT put_PostalCodes(
  [in] VARIANT vPostalCodes
);
```


</dt> </dl> </dd> <dt>

**Perfil**
</dt> <dd> <dl>

O caminho para o perfil do usuário.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Profile(
  [out] BSTR* pbstrProfile
);
HRESULT put_Profile(
  [in] BSTR bstrProfile
);
```


</dt> </dl> </dd> <dt>

**RequireUniquePassword**
</dt> <dd> <dl>

Um sinalizador que indica se uma nova senha deve ser diferente daquelas conhecidas por meio de um histórico de senhas.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **booliana**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RequireUniquePassword(
  [out] VARIANT_BOOL* pfRequireUniquePassword
);
HRESULT put_RequireUniquePassword(
  [in] VARIANT_BOOL fRequireUniquePassword
);
```


</dt> </dl> </dd> <dt>

**SeeAlso**
</dt> <dd> <dl>

Uma matriz de ADsPaths de outros objetos relacionados ao usuário.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

**TelephoneHome**
</dt> <dd> <dl>

Uma matriz de números de telefone página principal do usuário. No Active Directory, essa propriedade tem valor único e a matriz tem um elemento .

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneHome(
  [out] VARIANT* pvarTelephoneHome
);
HRESULT put_TelephoneHome(
  [in] VARIANT varTelephoneHome
);
```


</dt> </dl> </dd> <dt>

**TelephoneMobile**
</dt> <dd> <dl>

Uma matriz de números de telefone celular do usuário. No Active Directory, essa propriedade tem valor único e a matriz tem apenas um elemento.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneMobile(
  [out] VARIANT* pvarTelephoneMobile
);
HRESULT put_TelephoneMobile(
  [in] VARIANT varTelephoneMobile
);
```


</dt> </dl> </dd> <dt>

**Telephonenumber**
</dt> <dd> <dl>

Uma matriz de números de telefone, geralmente relacionados ao trabalho, associados ao usuário. No Active Directory, essa propriedade tem valor único e a matriz é de um único elemento.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] VARIANT* pvarTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] VARIANT varTelephoneNumber
);
```


</dt> </dl> </dd> <dt>

**TelephonePager**
</dt> <dd> <dl>

Uma matriz de números de pager do usuário. Em Active Directory essa propriedade é de valor único e a matriz é de um único elemento.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephonePager(
  [out] VARIANT* pvarTelephonePager
);
HRESULT put_TelephonePager(
  [in] VARIANT varTelephonePager
);
```


</dt> </dl> </dd> <dt>

**Título**
</dt> <dd> <dl>

O título do usuário.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Title(
  [out] BSTR* pbstrTitle
);
HRESULT put_Title(
  [in] BSTR bstrTitle
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentários

O provedor WinNT fornecido pela Microsoft não oferece suporte a todos os métodos de propriedade [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) , conforme apresentado acima. No entanto, o provedor dá suporte a outras propriedades que podem ser acessadas usando o método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) . Para obter mais informações e uma lista de propriedades sem suporte e exemplos de código, consulte [WinNT User Object](winnt-user-object.md) in [ADSI WinNT Provider](adsi-winnt-provider.md).

Para obter mais informações sobre recursos específicos do provedor LDAP ADSI do objeto de classe de usuário, consulte [objeto de usuário LDAP](ldap-user-object.md) no [provedor LDAP ADSI](adsi-ldap-provider.md). O tópico inclui [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), bem como exemplos de código para gerenciar uma conta de usuário.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como associar a um objeto de conta de usuário e recuperar o nome completo do usuário.


```VB
Dim usr As IADsUser
Dim sFullName as String

On Error GoTo Cleanup
Set usr = GetObject("WinNT://Fabrikam/JeffSmith,user")
sFullName = usr.FullName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



O exemplo de código a seguir mostra como associar a um objeto de conta de usuário e recuperar o nome completo do usuário.


```C++
IADsUser *GetUserObject(LPWSTR uPath)
{
    IADsUser *pUser;
    HRESULT hr = ADsGetObject(uPath,IID_IADsUser,(void**)&pUser);
    if (FAILED(hr)) {return NULL;}
    BSTR bstr;
    hr = pUser->get_FullName(&bstr);
    printf("User: %S\n", bstr);
    SysFreeString(bstr);
    return pUser;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsUser é definido como 3E37E320-17E2-11CF-ABC4-02608C9E7553<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)
</dt> <dt>

[Métodos de propriedade de interface](interface-property-methods.md)
</dt> <dt>

[**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get)
</dt> <dt>

[**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put)
</dt> <dt>

[Objeto de usuário do WinNT](winnt-user-object.md)
</dt> <dt>

[Provedor ADSI de WinNT](adsi-winnt-provider.md)
</dt> <dt>

[Objeto de usuário LDAP](ldap-user-object.md)
</dt> <dt>

[Provedor LDAP ADSI](adsi-ldap-provider.md)
</dt> </dl>

 

 





