---
description: Inicia o compartilhamento para um recurso de servidor.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Criar método da classe Win32_Share classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 582e255223b6eb971fd447c7884ff730662a1b344c107791b1a57a074c2c1354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504766"
---
# <a name="create-method-of-the-win32_share-class"></a>Criar método da classe Win32 \_ Share

O **método criar**   [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) inicia o compartilhamento para um recurso de servidor.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho* \[ Em\]
</dt> <dd>

Caminho local do compartilhamento Windows dados.

Exemplo, "C: \\ Arquivos de Programas".

</dd> <dt>

*Nome* \[ Em\]
</dt> <dd>

Passa o alias para um caminho definido como um compartilhamento em um sistema de computador executando Windows.

Exemplo, "public".

</dd> <dt>

*Tipo* \[ Em\]
</dt> <dd>

Passa o tipo de recurso que está sendo compartilhado. Os tipos incluem unidades de disco, filas de impressão, IPC (comunicações entre processos) e dispositivos gerais. Pode ser um dos valores a seguir.

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Unidade de disco** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Fila de Impressão** (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Dispositivo** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Administrador de unidade de** disco (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Imprimir Administrador de Filas** (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Administrador do** dispositivo (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**Administrador de IPC** (2147483651)


</dt> <dd></dd> </dl> </dd> <dt>

*MaximumAllowed* \[ in, opcional\]
</dt> <dd>

Limite o número máximo de usuários permitidos para usar esse recurso simultaneamente.

Exemplo: 10. Esse parâmetro é opcional.

</dd> <dt>

*Descrição* \[ in, opcional\]
</dt> <dd>

Comentário opcional para descrever o recurso que está sendo compartilhado. Esse parâmetro é opcional.

</dd> <dt>

*Senha* \[ in, opcional\]
</dt> <dd>

Senha (quando o servidor está em execução com segurança em nível de compartilhamento) para o recurso compartilhado. Se o servidor estiver em execução com segurança no nível do usuário, esse parâmetro será ignorado. Esse parâmetro é opcional.

</dd> <dt>

*Acesso* \[ in, opcional\]
</dt> <dd>

Descritor de segurança para permissões no nível do usuário. Um descritor de segurança contém informações sobre as permissões, o proprietário e os recursos de acesso do recurso. Se esse parâmetro não for fornecido ou for **NULL,** Todos terão acesso de leitura ao compartilhamento. Para obter mais informações, consulte [**Win32 \_ SecurityDescriptor e**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Alterando a segurança [de acesso em objetos securáveis.](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Nome inválido** (9)
</dt> <dt>

**Nível inválido** (10)
</dt> <dt>

**Parâmetro inválido** (21)
</dt> <dt>

**Compartilhamento duplicado** (22)
</dt> <dt>

**Caminho redirecionado** (23)
</dt> <dt>

**Dispositivo ou diretório desconhecido** (24)
</dt> <dt>

**Nome líquido não encontrado** (25)
</dt> <dt>

**Outros** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

**Create** é um método estático.

Somente os membros do grupo local Administradores ou Operadores de Conta ou aqueles com associação ao grupo de operadores Comunicação, Impressão ou Servidor podem executar Criar com **êxito.** O operador Print só pode adicionar filas de impressora. O operador Comunicação só pode adicionar filas de dispositivo de comunicação.

## <a name="examples"></a>Exemplos

O [exemplo Exportar e Importar Arquivos compartilha o](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell exporta e importa compartilhamentos de arquivos e define permissões de compartilhamento. Da mesma forma, [o exemplo Criar um compartilhamento](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) e definir permissões também cria um novo compartilhamento e define as permissões de compartilhamento.

O código do PowerShell a seguir cria um compartilhamento.


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



O exemplo de código anterior retorna o seguinte:

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

O exemplo de código C \# a seguir descreve como chamar o método create.


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Compartilhamento \_ win32**](win32-share.md)
</dt> </dl>

 

