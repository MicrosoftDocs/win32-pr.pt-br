---
description: Permite que um cliente gerencie as configurações de cota de disco global de um volume NTFS. Esse objeto disponibiliza a funcionalidade essencial da interface DIDiskQuotaUser para scripts e aplicativos baseados Visual Basic Microsoft.
title: Objeto DIDiskQuotaUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: b370056f40320561a38b1f77fbcf9a53ee35686a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843237"
---
# <a name="didiskquotauser-object"></a>Objeto DIDiskQuotaUser

Permite que um cliente gerencie as configurações de cota de disco global de um volume NTFS. Esse objeto disponibiliza a funcionalidade essencial da interface **DIDiskQuotaUser** para scripts e aplicativos baseados Visual Basic Microsoft.

## <a name="members"></a>Membros

O **objeto DIDiskQuotaUser** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto DIDiskQuotaUser** tem esses métodos.



| Método                                           | Descrição                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [**Invalidate**](didiskquotauser-invalidate.md) | Limpa as informações de usuário armazenadas em cache do objeto.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto DIDiskQuotaUser** tem essas propriedades.



| Propriedade                                                                        | Tipo de acesso           | Descrição                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**AccountContainerName**](didiskquotauser-accountcontainername.md)<br/> | Somente leitura<br/>  | Obtém o nome do contêiner da conta do usuário.<br/>                                            |
| [**AccountStatus**](didiskquotauser-accountstatus.md)<br/>               | Somente leitura<br/>  | Obtém o status da conta do usuário.<br/>                                                    |
| [**DisplayName**](didiskquotauser-displayname.md)<br/>                   | Somente leitura<br/>  | Obtém o nome de exibição do usuário.<br/>                                                             |
| [**ID**](didiskquotauser-id.md)<br/>                                     | Somente leitura<br/>  | Obtém uma ID que identifica exclusivamente o usuário.<br/>                                             |
| [**LogonName**](didiskquotauser-logonname.md)<br/>                       | Somente leitura<br/>  | Obtém o nome da conta de logon do usuário.<br/>                                                       |
| [**QuotaLimit**](didiskquotauser-quotalimit.md)<br/>                     | Leitura/gravação<br/> | Define ou obtém o limite de cota [**atual do usuário.**](diskquotacontrol-object.md)<br/>           |
| [**QuotaLimitText**](didiskquotauser-quotalimittext.md)<br/>             | Somente leitura<br/>  | Obtém o [**limite de cota**](diskquotacontrol-object.md) atual do usuário como uma cadeia de texto. <br/> |
| [**QuotaThreshold**](didiskquotauser-quotathreshold.md)<br/>             | Leitura/gravação<br/> | Define ou Obtém o limite de aviso do usuário, em bytes.<br/>                                      |
| [**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)<br/>     | Somente leitura<br/>  | Obtém o limite de aviso do usuário como uma cadeia de texto.<br/>                                       |
| [**QuotaUsed**](didiskquotauser-quotaused.md)<br/>                       | Somente leitura<br/>  | Obtém o uso do disco atual do usuário, em bytes.<br/>                                             |
| [**QuotaUsedText**](didiskquotauser-quotausedtext.md)<br/>               | Somente leitura<br/>  | Obtém o uso do disco atual do usuário como uma cadeia de texto.<br/>                                      |



 

## <a name="remarks"></a>Comentários

Cada usuário no volume que é gerenciado pelo objeto [**DiskQuotaControl**](diskquotacontrol-object.md) tem um objeto **DIDiskQuotaUser** associado a ele. Esse objeto permite que um cliente gerencie as configurações de um usuário individual. Há várias maneiras de obter o objeto **DIDiskQuotaUser** de um usuário:

-   Os objetos **DIDiskQuotaUser** para todos os usuários com cotas no volume são expostos como uma coleção e podem ser enumerados. Uma discussão sobre como enumerar objetos **DIDiskQuotaUser** é encontrada abaixo.
-   Quando você adiciona um novo usuário, o método [**adduser**](diskquotacontrol-adduser.md) retorna o objeto **DIDiskQuotaUser** do usuário.
-   Se você tiver o nome do usuário, o método [**FindUser**](diskquotacontrol-finduser.md) retornará o objeto **DIDiskQuotaUser** do usuário.

### <a name="enumerating-disk-quota-users"></a>Enumerando usuários de cota de disco

Os objetos **DIDiskQuotaUser** para todos os usuários com uma cota no volume são expostos como uma coleção. O objeto [**DiskQuotaControl**](diskquotacontrol-object.md) exporta um método enumerador padrão que permite enumerar a coleção de objetos **DIDiskQuotaUser** . O procedimento a seguir ilustra como executar a enumeração com o Microsoft JScript (compatível com a especificação de linguagem ECMA 262). Você pode usar um procedimento semelhante com o Visual Basic ou o Microsoft Visual Basic Scripting Edition (VBScript).

1.  Crie um novo [**objeto DiskQuotaControl.**](diskquotacontrol-object.md)
2.  Inicialize-o com [**Inicializar**](diskquotacontrol-initialize.md).
3.  Crie um novo objeto **enumerador JScript.**
4.  Use um loop **for** para enumerar os **objetos DIDiskQuotaUser.** Não é necessário definir um valor inicial. O método **moveNext** do objeto enumerador notifica o método **de item** para retornar o próximo **objeto DIDiskQuotaUser.** O **método atEnd** retorna **false** quando você chega ao final da lista.
5.  Conforme necessário, use o objeto **DIDiskQuotaUser** retornado pelo método **de item** do enumerador para recuperar ou definir uma ou mais das propriedades de cota de disco do usuário associado.

O fragmento de código a seguir ilustra como enumerar objetos **DIDiskQuotaUser** com JScript. O **argumento \_ Rótulo** de Volume passado para a **função EnumUsers** é um valor de cadeia de caracteres que contém um rótulo de volume como "C: \\ \\ ".


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Shell**](shell.md)
</dt> </dl>

 

 




