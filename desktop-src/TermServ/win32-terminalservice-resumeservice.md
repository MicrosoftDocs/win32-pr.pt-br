---
title: Método ResumeService da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Método ResumeService da classe Win32_Service (Serviços de Área de Trabalho Remota) – tenta colocar o serviço referenciado no estado retomado.
ms.assetid: AA020A0A-E69C-44AB-B259-A73460728770
ms.tgt_platform: multiple
keywords:
- Método ResumeService Serviços de Área de Trabalho Remota
- Método ResumeService Serviços de Área de Trabalho Remota classe , Win32_Service classe
- Win32_Service classe Serviços de Área de Trabalho Remota , método ResumeService
topic_type:
- apiref
api_name:
- Win32_Service.ResumeService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2886e011bddd4aa45a8d0fcf3041e54d93487a3d4835cd85dcd1f5fb3de3955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867856"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a>Método ResumeService da classe Win32_Service (Serviços de Área de Trabalho Remota)

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tenta colocar o serviço referenciado no estado retomado.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ResumeService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**0**
</dt> <dd>

A solicitação foi aceita.

</dd> <dt>

**1**
</dt> <dd>

A solicitação não terá suporte.

</dd> <dt>

**2**
</dt> <dd>

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

O código de controle solicitado não pode ser enviado para o serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**A** propriedade State) é igual a 0, 1 ou 2.

</dd> <dt>

**6**
</dt> <dd>

O serviço não foi iniciado.

</dd> <dt>

**7**
</dt> <dd>

O serviço não respondeu à solicitação de início em um tempo oportuno.

</dd> <dt>

**8**
</dt> <dd>

Falha desconhecida ao iniciar o serviço.

</dd> <dt>

**9**
</dt> <dd>

O caminho do diretório para o arquivo executável de serviço não foi encontrado.

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

Uma dependência de que esse serviço depende foi removida do sistema.

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

Esse serviço está sendo removido do sistema.

</dd> <dt>

**17**
</dt> <dd>

O serviço não tem nenhum thread de execução.

</dd> <dt>

**18**
</dt> <dd>

O serviço tem dependências circulares quando ele é iniciado.

</dd> <dt>

**19**
</dt> <dd>

Um serviço está em execução com o mesmo nome.

</dd> <dt>

**20**
</dt> <dd>

O nome do serviço tem caracteres inválidos.

</dd> <dt>

**21**
</dt> <dd>

Parâmetros inválidos foram passados para o serviço.

</dd> <dt>

**22**
</dt> <dd>

A conta na qual esse serviço é executado é inválida ou não tem as permissões para executar o serviço.

</dd> <dt>

**23**
</dt> <dd>

O serviço existe no banco de dados de serviços disponível no sistema.

</dd> <dt>

**24**
</dt> <dd>

O serviço está pausado atualmente no sistema.

</dd> </dl>

## <a name="remarks"></a>Comentários

Embora possa parecer não haver nenhuma diferença prática entre um serviço que está parado e um serviço que está em pausa, os dois estados aparecem de forma diferente para o SCM. Um serviço parado é um serviço que não está em execução e deve passar por todo o procedimento de início do serviço. Um serviço em pausa, no entanto, ainda está em execução, mas teve seu funcionamento suspenso. Por isso, um serviço em pausa não precisa passar por todo o procedimento de início do serviço, mas precisa de um procedimento diferente para retomar o funcionamento.

Você deve usar o método adequado para iniciar um serviço que foi interrompido ou para retomar um serviço que foi pausado. Os [**métodos do \_ Serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) [**StartService**](win32-terminalservice-startservice.md) e **ResumeService** devem ser usados nas seguintes situações:

-   Se um serviço estiver parado no momento, você deverá usar o [**método StartService**](win32-terminalservice-startservice.md) para reiniciá-lo; **ResumeService** não pode iniciar um serviço que está parado no momento.
-   Se um serviço estiver em pausa, você deverá usar **ResumeService**. Se você usar o [**método StartService**](win32-terminalservice-startservice.md) em um serviço em pausa, receberá a mensagem "O serviço já está em execução". No entanto, o serviço permanece em pausa até que o código de controle de serviço de retomada seja enviado a ele.

## <a name="examples"></a>Exemplos

O [exemplo Retomar Serviços de Início Automático com](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript em Pausa reinicia todos os serviços de início automático que foram pausados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Serviço \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Classes do sistema operacional](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[Tarefas WMI: Serviços](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

