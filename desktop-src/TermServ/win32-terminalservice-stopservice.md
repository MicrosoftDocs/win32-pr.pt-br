---
title: Método StopService da classe Win32_Service (Sdoias. h) (serviço de terminal)
description: Coloca o serviço, representado pelo \_ objeto TerminalService do Win32, no estado parado.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- Método StopService Serviços de Área de Trabalho Remota
- Método StopService Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método StopService
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105778802"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a>Método StopService da classe de Win32_Service (Sdoias. h) para o serviço de terminal

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca o serviço, representado pelo [**objeto \_ TerminalService do Win32**](win32-terminalservice.md) , no estado parado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

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

O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**** A propriedade State) é igual a 0, 1 ou 2.

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

**Abril**
</dt> <dd>

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

</dd> </dl>

## <a name="remarks"></a>Comentários

Depois de determinar quais serviços podem ser interrompidos ou pausados, você pode usar os métodos **StopService** e [**PauseService**](win32-terminalservice-pauseservice.md) para parar e pausar serviços. A decisão de interromper um serviço em vez de pausá-lo, ou vice-versa, depende de vários fatores, incluindo o seguinte:

-   O serviço é capaz de ser pausado? Caso contrário, sua única opção é parar o serviço.
-   Você precisa continuar tratando as solicitações do cliente para qualquer pessoa já conectada ao serviço? Nesse caso, pausar um serviço geralmente permite que ele manipule clientes existentes enquanto nega acesso a novos clientes. Por outro lado, quando você interrompe um serviço, todos os clientes são imediatamente desconectados.
-   Você precisa reconfigurar um serviço e fazer com que as alterações entrem em vigor imediatamente? Embora as propriedades do serviço possam ser alteradas enquanto um serviço é pausado, a maioria delas não tem efeito até que o serviço seja realmente interrompido e reiniciado.

O código de script necessário para interromper um serviço é quase idêntico ao código necessário para pausar o serviço.

Se você tentar interromper um serviço que tem serviços dependentes em execução, o método **StopService** falhará com um valor de retorno de 3. Os serviços dependentes devem ser interrompidos primeiro.

Se você parar um serviço, verifique imediatamente o [**\_ TerminalService do Win32**](win32-terminalservice.md).**** A propriedade State, pois o valor ainda pode mostrar o serviço como em execução.

## <a name="examples"></a>Exemplos

[O set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) O exemplo do PowerShell define o estado do serviço para máquinas remotas.

O exemplo de [parar um serviço e seus dependentes](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) do VBScript interrompe um serviço e todos os serviços dependentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Classes do sistema operacional](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[Tarefas do WMI: serviços](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**PauseService**](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

