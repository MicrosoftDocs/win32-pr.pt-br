---
description: Método SetSecurityDescriptor da classe Win32_Service (provedores WMI CIMWin32) – grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20619a459171841d0a3bd5b7acabe984dc835dac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099994"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método SetSecurityDescriptor da classe Win32_Service (provedores WMI CIMWin32)

O método **SetSecurityDescriptor** grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descritor* \[ no\]
</dt> <dd>

O descritor de segurança associado ao serviço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Êxito**
</dt> <dd>

0

A solicitação foi aceita.

</dd> <dt>

**1**
</dt> <dd>

A solicitação não terá suporte.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

O usuário não tinha o acesso necessário.

</dd> <dt>

**3**
</dt> <dd>

O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.

</dd> <dt>

**4**
</dt> <dd>

O código de controle pedido não é válido ou é inaceitável para o serviço.

</dd> <dt>

**5**
</dt> <dd>

O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).**** A propriedade State) é igual a 0, 1 ou 2.

</dd> <dt>

**6**
</dt> <dd>

O serviço não foi iniciado.

</dd> <dt>

**7**
</dt> <dd>

O serviço não respondeu à solicitação de início em um tempo oportuno.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

8

Falha desconhecida ao iniciar o serviço.

</dd> <dt>

**Privilégio ausente**
</dt> <dd>

9

O caminho do diretório para o arquivo executável do serviço não foi encontrado.

</dd> <dt>

**10**
</dt> <dd>

O serviço já está em execução.

</dd> <dt>

**11**
</dt> <dd>

O banco de dados para adicionar um serviço novo está bloqueado.

</dd> <dt>

**12**
</dt> <dd>

Uma dependência da qual esse serviço depende foi removida do sistema.

</dd> <dt>

**13**
</dt> <dd>

O serviço não localizou o serviço necessário em um serviço dependente.

</dd> <dt>

**14**
</dt> <dd>

O serviço foi desabilitado do sistema.

</dd> <dt>

**15**
</dt> <dd>

O serviço não tem a autenticação correta para ser executado no sistema.

</dd> <dt>

**16**
</dt> <dd>

Este serviço está sendo removido do sistema.

</dd> <dt>

**17**
</dt> <dd>

O serviço não tem nenhum thread de execução.

</dd> <dt>

**anos**
</dt> <dd>

O serviço tem dependências circulares quando é iniciado.

</dd> <dt>

**aprimora**
</dt> <dd>

Um serviço está sendo executado com o mesmo nome.

</dd> <dt>

**20**
</dt> <dd>

O nome do serviço tem caracteres inválidos.

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

21

Parâmetros inválidos foram passados para o serviço.

</dd> <dt>

**22**
</dt> <dd>

A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.

</dd> <dt>

**23**
</dt> <dd>

O serviço existe no banco de dados de serviços disponível no sistema.

</dd> <dt>

**24**
</dt> <dd>

O serviço está pausado atualmente no sistema.

</dd> <dt>

**Outros**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema. Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado. Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).

Você pode atualizar a DACL e a SACL na instância [**\_ SecurityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ao chamar esse método, mas também pode atualizar apenas a DACL ou apenas a SACL.

Os valores a seguir [**no \_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) determinam se a DACL, a SACL ou ambas são atualizadas.

-   **\_DACL \_ presente**

    Indica que a DACL deve ser atualizada. Se isso não for definido, o WMI preservará o valor original da DACL.

-   **\_SACL \_ presente**

    Indica que a SACL deve ser atualizada. Se isso não for definido, o WMI preservará o valor original da SACL. Para atualizar a SACL, a conta deve ter o privilégio **SeSecurityPrivilege** habilitado. Para scripts, o nome do privilégio é **SeSecurityPrivilege**. Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants).

Se o grupo de confiança e as propriedades de confiança do proprietário não forem **nulas**, eles serão atualizados. Caso contrário, o WMI preservará os valores originais. Para obter mais informações, consulte [objetos do descritor de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).

Quando uma nova SACL é **nula** em uma chamada desse método, a SACL do descritor de segurança no objeto protegível de destino permanece inalterada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_Serviço Win32**](win32-service.md)
</dt> <dt>

[**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objetos do descritor de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Alterando a segurança de acesso em objetos protegíveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

