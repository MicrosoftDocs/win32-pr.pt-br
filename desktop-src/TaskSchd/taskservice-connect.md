---
title: Método TaskService. Connect
description: Para scripts, o se conecta a um computador remoto e associa todas as chamadas subsequentes nessa interface a uma sessão remota.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Agendador de Tarefas do método Connect
- Método Connect Agendador de Tarefas, objeto TaskService
- Agendador de Tarefas de objeto TaskService, método Connect
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918212"
---
# <a name="taskserviceconnect-method"></a>Método TaskService. Connect

Para scripts, o se conecta a um computador remoto e associa todas as chamadas subsequentes nessa interface a uma sessão remota. Se o parâmetro ServerName estiver vazio, esse método será executado no computador local. Se a userId não for especificada, o token atual será usado.

## <a name="syntax"></a>Sintaxe


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do Server* \[ em, opcional\]
</dt> <dd>

O nome do computador ao qual você deseja se conectar. Se o parâmetro ServerName estiver vazio, esse método será executado no computador local.

</dd> <dt>

*usuário* \[ do em, opcional\]
</dt> <dd>

O nome de usuário que é usado durante a conexão com o computador. Se o usuário não for especificado, o token atual será usado.

</dd> <dt>

*domínio* \[ do em, opcional\]
</dt> <dd>

O domínio do usuário especificado no parâmetro *User* .

</dd> <dt>

*senha* \[ do em, opcional\]
</dt> <dd>

A senha usada para se conectar ao computador. Se o nome de usuário e a senha não forem especificados, o token atual será usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **TaskService. Connect** deve ser chamado antes de chamar qualquer um dos outros métodos [**TaskService**](taskservice.md) .

Se o método Connect falhar, você poderá coletar o identificador de erro para localizar o significado do erro. A tabela a seguir lista os identificadores de erro e suas descrições.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificador de erro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x80070005</td>
<td>Acesso negado para se conectar ao serviço de Agendador de Tarefas.</td>
</tr>
<tr class="even">
<td>0x80041315</td>
<td>O serviço de Agendador de Tarefas não está em execução.</td>
</tr>
<tr class="odd">
<td>0x8007000e</td>
<td>O aplicativo não tem memória suficiente para concluir a operação ou o <em>usuário</em>, a <em>senha</em>ou o <em>domínio</em> tem pelo menos um valor nulo e um não nulo.</td>
</tr>
<tr class="even">
<td>53</td>
<td>Esse erro é retornado nas seguintes situações:
<ul>
<li>O nome do computador especificado no parâmetro <em>ServerName</em> não existe.</li>
<li>Quando você está tentando se conectar a um computador com Windows Server 2003 ou Windows XP, o computador remoto não tem a exceção de firewall de compartilhamento de arquivos e impressoras habilitada ou o serviço de registro remoto não está em execução.</li>
<li>Quando você estiver tentando se conectar a um computador com Windows Vista e o computador remoto não tiver a exceção de firewall de gerenciamento de tarefas agendadas remotas habilitada e a exceção de firewall de compartilhamento de arquivos e impressoras estiver habilitada ou o serviço de registro remoto não estiver em execução.</li>
</ul></td>
</tr>
<tr class="odd">
<td>50</td>
<td>Os parâmetros de <em>usuário</em>, <em>senha</em>ou <em>domínio</em> não podem ser especificados ao se conectar a um computador remoto com Windows XP ou Windows Server 2003 de um computador com Windows Vista.</td>
</tr>
</tbody>
</table>



 

Se você estiver se conectando a um computador remoto com Windows Vista de um Windows Vista, será necessário permitir a exceção de firewall de gerenciamento de tarefas agendadas remotas no computador remoto. Para permitir essa exceção, clique em Iniciar, painel de controle, segurança, permitir um programa pelo firewall do Windows e marque a caixa de seleção gerenciamento remoto de tarefas agendadas. Em seguida, clique no botão OK na caixa de diálogo Configurações do firewall do Windows.

Se você estiver se conectando a um computador remoto com Windows XP ou Windows Server 2003 de um computador com Windows Vista, será necessário permitir a exceção de firewall de compartilhamento de arquivos e impressoras no computador remoto. Para permitir essa exceção, clique em Iniciar, painel de controle, clique duas vezes em Firewall do Windows, selecione a guia exceções e selecione a exceção de firewall de compartilhamento de arquivos e impressoras. Em seguida, clique no botão OK na caixa de diálogo Firewall do Windows. O serviço registro remoto também deve estar em execução no computador remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





