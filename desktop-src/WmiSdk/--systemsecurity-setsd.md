---
description: Define o descritor de segurança para o namespace ao qual um usuário está conectado. Esse método requer um descritor de segurança em formato de matriz de bytes binários. Se você estiver escrevendo um script, use o método SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Método definido da classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813018"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>Método SetS da \_ \_ classe SystemSecurity

O método **sets** define o descritor de segurança para o namespace ao qual um usuário está conectado. Esse método requer um descritor de segurança em formato de matriz de bytes binários. Se você estiver escrevendo um script, use o método [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) . Para obter mais informações, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

Se você estiver programando em C++, poderá manipular o descritor de segurança binário usando [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e os métodos de conversão [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Um usuário deve ter a permissão **Write \_ DAC** e, por padrão, um administrador tem essa permissão. A única parte do descritor de segurança que é usada é a ACE (entrada de controle de acesso) não herdada na DACL (lista de controle de acesso discricionário). Ao definir o sinalizador de **\_ herança de contêiner** nas Aces, o descritor de segurança afeta os namespaces filho. As ACEs allow e Deny são permitidas.

> [!Note]  
> Como Deny e Allow ACEs são permitidas em uma DACL, a ordem das ACEs é importante. Para obter mais informações, consulte [ordenando ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

## <a name="syntax"></a>Sintaxe


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SD* \[ no\]
</dt> <dd>

Matriz de bytes que compõe o descritor de segurança.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um **HRESULT** que indica o status de uma chamada de método. Para aplicativos de script e Visual Basic, o resultado pode ser obtido de [Parameters. ReturnValue](parsing-outparameters-objects.md). Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

A lista a seguir lista os valores de retorno que são significativos para **conjuntos**.

<dl> <dt>

**S \_ OK**
</dt> <dd>

Método executado com êxito.

</dd> <dt>

**acesso ao WBEM \_ E \_ \_ negado**
</dt> <dd>

O chamador não tem direitos suficientes para chamar este método.

</dd> <dt>

**\_método WBEM \_ E \_ desabilitado**
</dt> <dd>

Tentativa de executar este método no sistema operacional que não oferece suporte a ele.

</dd> <dt>

**\_objeto WBEM E \_ inválido \_**
</dt> <dd>

O SD não passa por testes de validade básicos.

</dd> <dt>

**parâmetro de WBEM \_ E \_ inválido \_**
</dt> <dd>

O SD não é válido devido a um dos seguintes:

-   A DACL está ausente.
-   A DACL não é válida.
-   ACE tem o sinalizador de **\_ \_ \_ representante de gravação completa de WBEM** definido e o sinalizador de **\_ \_ \_ Representante** de gravação parcial do WBEM ou do **\_ \_ provedor de gravação** do WBEM não está definido.
-   ACE tem o **sinalizador \_ \_ ACE somente Inherit** definido sem o **sinalizador \_ \_ Ace Inherit do contêiner** .
-   ACE tem um conjunto de bits de acesso desconhecido.
-   ACE tem um sinalizador definido que não está na tabela.
-   ACE tem um tipo que não está na tabela.
-   O proprietário e o grupo estão ausentes no SD.

Para obter mais informações sobre os sinalizadores de ACE (entrada de controle de acesso), consulte [constantes de segurança do WMI](wmi-security-constants.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter mais informações sobre como modificar a segurança do namespace de forma programática ou manual, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Exemplos

O script a seguir mostra como usar o **sets** para definir o descritor de segurança do namespace para o namespace raiz e alterá-lo para a matriz de bytes mostrada em *strSD*.


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



O exemplo de código C# a seguir usa System. Security. AccessControl. RawSecurityDescriptor para enumerar, inserir e remover novos objetos CommonAce em RawSecurityDescriptor. DiscretionaryAcl e, em seguida, convertê-lo novamente em uma matriz de bytes para salvá-lo por meio de SetS. Um SecurityIdentifier pode ser recuperado usando NTAccount e translate.


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity:: Obtém-se**](--systemsecurity-getsd.md)
</dt> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[**Ace do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protegendo namespaces WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

