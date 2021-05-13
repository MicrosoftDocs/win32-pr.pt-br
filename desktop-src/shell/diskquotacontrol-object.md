---
description: Permite que um administrador gerencie as propriedades de cota de disco de um volume.
title: Objeto DiskQuotaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841547"
---
# <a name="diskquotacontrol-object"></a>Objeto DiskQuotaControl

Permite que um administrador gerencie as propriedades de cota de disco de um volume. O sistema de arquivos NTFS permite que um administrador gerencie o uso de disco em um volume compartilhado alocando uma quantidade especificada de espaço em disco ou limite de cota *para* cada usuário. Você pode usar esse objeto para definir o limite de cota padrão que será atribuído automaticamente a todos os novos usuários.

## <a name="members"></a>Membros

O **objeto DiskQuotaControl** tem estes tipos de membros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

O **objeto DiskQuotaControl** tem esses eventos.



| Evento                                                           | Descrição                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) | Ocorre quando as informações de nome de [**um objeto DIDiskQuotaUser**](didiskquotauser-object.md) foram resolvidas.<br/> |



 

### <a name="methods"></a>Métodos

O **objeto DiskQuotaControl** tem esses métodos.



| Método                                                                                    | Descrição                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**AddUser**](diskquotacontrol-adduser.md)                                               | Atribui uma cota de disco não padrão a um novo usuário.<br/>                                  |
| [**DeleteUser**](diskquotacontrol-deleteuser.md)                                         | Exclui um usuário do volume.<br/>                                                 |
| [**FindUser**](diskquotacontrol-finduser.md)                                             | Localiza a entrada de um usuário, por nome, no arquivo de cota do volume.<br/>                      |
| [**GiveUserNameResolutionPriority**](diskquotacontrol-giveusernameresolutionpriority.md) | Coloca o objeto de usuário especificado ao lado na linha para resolução de nomes.<br/>              |
| [**Inicializar**](diskquotacontrol-initialize.md)                                         | Abre um volume especificado e inicializa seu objeto de controle de cota.<br/>              |
| [**InvalidateSidNameCache**](diskquotacontrol-invalidatesidnamecache.md)                 | Invalida o cache de nome de usuário da ID de segurança.<br/>                                    |
| [**ShutdownNameResolution**](diskquotacontrol-shutdownnameresolution.md)                 | Desliga o thread de resolução de nomes de usuário.<br/>                                     |
| [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md)               | Traduz um nome de logon para a ID de segurança de usuário correspondente no formato de cadeia de caracteres.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **DiskQuotaControl** tem essas propriedades.



| Propriedade                                                                                   | Tipo de acesso           | Descrição                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)<br/>                 | Leitura/gravação<br/> | Define ou Obtém o limite de cota padrão.<br/>                                                                                                              |
| [**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)<br/>         | Somente leitura<br/>  | Obtém o limite de cota padrão como uma cadeia de texto.<br/>                                                                                                     |
| [**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)<br/>         | Leitura/gravação<br/> | Define ou Obtém o limite de cota padrão.<br/>                                                                                                          |
| [**DefaultQuotaThresholdText**](diskquotacontrol-defaultquotathresholdtext.md)<br/> | Somente leitura<br/>  | Obtém o limite de cota padrão como uma cadeia de texto.<br/>                                                                                                 |
| [**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)<br/>                         | Leitura/gravação<br/> | Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.<br/>     |
| [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)<br/>                 | Leitura/gravação<br/> | Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.<br/> |
| [**QuotaFileIncomplete**](diskquotacontrol-quotafileincomplete.md)<br/>             | Somente leitura<br/>  | Obtém um valor booliano que indica se o arquivo de cota do volume está concluído.<br/>                                                             |
| [**QuotaFileRebuilding**](diskquotacontrol-quotafilerebuilding.md)<br/>             | Somente leitura<br/>  | Obtém um valor booliana que indica se o arquivo de cota para o volume está sendo reconstruído no momento.<br/>                                              |
| [**QuotaState**](diskquotacontrol-quotastate.md)<br/>                               | Leitura/gravação<br/> | Define ou obtém o estado das cotas de disco do volume.<br/>                                                                                                |
| [**UserNameResolution**](diskquotacontrol-usernameresolution.md)<br/>               | Leitura/gravação<br/> | Define ou obtém um valor que controla como o SID do usuário é resolvido para nomes de usuário.<br/>                                                                        |



 

## <a name="remarks"></a>Comentários

Um administrador pode usar o **objeto DiskQuotaControl** para realizar várias tarefas, incluindo as seguintes:

-   Habilitando e desabilitando o sistema de cota de disco do volume.
-   Obtendo o status do sistema de cota no volume.
-   Negar espaço em disco para usuários que excedem o limite de cota.
-   Especificando os valores padrão de limite de aviso e limite de cota que serão atribuídos a novos usuários.
-   Adicionar e remover usuários.

O **objeto DiskQuotaControl** permite definir valores padrão globais para o volume para propriedades como limites de cota. No entanto, cada usuário é representado por [**um objeto DIDiskQuotaUser**](didiskquotauser-object.md) que pode ser usado para especificar configurações de cota individuais.

Há várias maneiras de obter o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) de um usuário:

-   Os [**objetos DIDiskQuotaUser**](didiskquotauser-object.md) para todos os usuários com cotas no volume são expostos como uma coleção e podem ser enumerados. Para uma discussão sobre como enumerar **objetos DIDiskQuotaUser,** consulte **Enumerando** usuários de cota de disco na seção Comentários de **DIDiskQuotaUser**.
-   Quando você adiciona um novo usuário, o [**método AddUser**](diskquotacontrol-adduser.md) retorna o objeto [**DIDiskQuotaUser do**](didiskquotauser-object.md) usuário.
-   Se você tiver o nome do usuário, o [**método FindUser**](diskquotacontrol-finduser.md) retornará o objeto [**DIDiskQuotaUser do**](didiskquotauser-object.md) usuário.

Esse objeto disponibiliza a funcionalidade essencial da interface IDiskQuotaControl para scripts e aplicativos baseados Visual Basic Microsoft.

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

 

 




