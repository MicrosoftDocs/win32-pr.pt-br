---
description: O método de classe WMI EnableStatic habilita o endereçamento TCP/IP estático para o adaptador de rede de destino. Como resultado, o DHCP para esse adaptador de rede está desabilitado.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Método EnableStatic da Win32_NetworkAdapterConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03d2c7214f9cfb89b8efcb612f3bc07840448ff0eaf1b064556d2797b74d4822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918416"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a>Método EnableStatic da classe \_ NetworkAdapterConfiguration do Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableStatic** habilita o endereçamento TCP/IP estático para o adaptador de rede de destino. Como resultado, o DHCP para esse adaptador de rede está desabilitado.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IPAddress* \[ Em\]
</dt> <dd>

Lista todos os endereços IP estáticos para o adaptador de rede atual.

Exemplo: 155.34.22.0.

</dd> <dt>

*SubnetMask* \[ Em\]
</dt> <dd>

Máscaras de sub-rede que complementam os valores no *parâmetro IPAddress.*

Exemplo: 255.255.0.0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (um) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro número se houver um erro. Para obter mais informações sobre códigos de erro, consulte [**Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Conclusão bem-sucedida, nenhuma reinicialização necessária**
</dt> <dd>

0

Conclusão bem-sucedida, sem necessidade de reinicialização.

</dd> <dt>

**Conclusão bem-sucedida, reinicialização necessária**
</dt> <dd>

1

Conclusão bem-sucedida, reinicialização necessária.

</dd> <dt>

**Método sem suporte nesta plataforma**
</dt> <dd>

64

Não há suporte para o método nesta plataforma.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

65

Falha desconhecida.

</dd> <dt>

**Máscara de sub-rede inválida**
</dt> <dd>

66

Máscara de sub-rede inválida.

</dd> <dt>

**Ocorreu um erro ao processar uma Instância que foi retornada**
</dt> <dd>

67

Ocorreu um erro ao processar uma instância que foi retornada.

</dd> <dt>

**Parâmetro de entrada inválido**
</dt> <dd>

68

Parâmetro de entrada inválido.

</dd> <dt>

**Mais de 5 gateways especificados**
</dt> <dd>

69

Mais de cinco gateways especificados.

</dd> <dt>

**Endereço IP inválido**
</dt> <dd>

70

Endereço IP inválido.

</dd> <dt>

**Endereço IP do gateway inválido**
</dt> <dd>

71

Endereço IP do gateway inválido.

</dd> <dt>

**Ocorreu um erro ao acessar o Registro para as informações solicitadas**
</dt> <dd>

72

Ocorreu um erro ao acessar o Registro para as informações solicitadas.

</dd> <dt>

**Nome de domínio inválido**
</dt> <dd>

73

Nome de domínio inválido.

</dd> <dt>

**Nome de host inválido**
</dt> <dd>

74

Nome de host inválido.

</dd> <dt>

**Nenhum servidor WINS primário/secundário definido**
</dt> <dd>

75

Nenhum servidor WINS primário ou secundário definido.

</dd> <dt>

**Arquivo inválido**
</dt> <dd>

76

Arquivo inválido.

</dd> <dt>

**Caminho do sistema inválido**
</dt> <dd>

77

Caminho do sistema inválido.

</dd> <dt>

**Falha na cópia do arquivo**
</dt> <dd>

78

Falha na cópia do arquivo.

</dd> <dt>

**Parâmetro de segurança inválido**
</dt> <dd>

79

Parâmetro de segurança inválido.

</dd> <dt>

**Não é possível configurar o serviço TCP/IP**
</dt> <dd>

80

Não é possível configurar o serviço TCP/IP.

</dd> <dt>

**Não é possível configurar o serviço DHCP**
</dt> <dd>

81

Não é possível configurar o serviço DHCP. Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

**Não é possível renovar a concessão de DHCP**
</dt> <dd>

82

Não é possível renovar a concessão de DHCP.

</dd> <dt>

**Não é possível liberar a concessão de DHCP**
</dt> <dd>

83

Não é possível liberar a concessão de DHCP.

</dd> <dt>

**IP não habilitado no adaptador**
</dt> <dd>

84

IP não habilitado no adaptador.

</dd> <dt>

**IPX não habilitado no adaptador**
</dt> <dd>

85

IPX não habilitado no adaptador.

</dd> <dt>

**Erro de limites de número de quadro/rede**
</dt> <dd>

86

Erro de limites de quadro ou número de rede.

</dd> <dt>

**Tipo de quadro inválido**
</dt> <dd>

87

Tipo de quadro inválido.

</dd> <dt>

**Número de rede inválido**
</dt> <dd>

88

Número de rede inválido.

</dd> <dt>

**Número de rede duplicado**
</dt> <dd>

89

Número de rede duplicado.

</dd> <dt>

**Parâmetro fora dos limites**
</dt> <dd>

90

Parâmetro fora dos limites.

</dd> <dt>

**Acesso negado**
</dt> <dd>

91

Acesso negado

</dd> <dt>

**Memória insuficiente**
</dt> <dd>

92

Sem memória.

</dd> <dt>

**Já existe**
</dt> <dd>

93

Já existe.

</dd> <dt>

**Caminho, arquivo ou objeto não encontrado**
</dt> <dd>

94

Caminho, arquivo ou objeto não encontrado.

</dd> <dt>

**Não é possível notificar o serviço**
</dt> <dd>

95

Não é possível notificar o serviço.

</dd> <dt>

**Não é possível notificar o serviço DNS**
</dt> <dd>

96

Não é possível notificar o serviço DNS.

</dd> <dt>

**Interface não configurável**
</dt> <dd>

97

Interface não configurável.

</dd> <dt>

**Nem todas as concessões DHCP podem ser liberadas/renovadas**
</dt> <dd>

98

Nem todas as concessões DHCP podem ser liberadas ou renovadas.

</dd> <dt>

**DHCP não habilitado no adaptador**
</dt> <dd>

100

O DHCP não está habilitado no adaptador.

</dd> <dt>

**2147786788**
</dt> <dd>

Bloqueio de gravação não habilitado. Para obter mais informações, [**consulte INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).

</dd> <dt>

**Outras**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao usar **EnableStatic** para alterar o endereço IP do computador remoto, enquanto estiver conectado por meio desse adaptador, você provavelmente perderá a conexão com o computador remoto e receberá uma mensagem de erro RPC não disponível. (no entanto, as configurações são alteradas). Para evitar esse cenário, considere alterar as configurações de Gateway e/ou DNS antes de definir o endereço IP do adaptador.

Ao usar **EnableStatic** para dar a um adaptador uma configuração de IP estático, a função retornará um "81 – Não é possível configurar o serviço DHCP" se o adaptador já estiver configurado com um endereço estático. No entanto, a função ainda tem êxito na configuração com a nova operação.

## <a name="examples"></a>Exemplos

O [IP estático e,](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) em seguida, ingressar em um exemplo de código do PowerShell de domínio, na Galeria do TechNet, usa **EnableStatic** para adicionar um IP estático a um computador local.

O [exemplo de código](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) Atribuir um endereço IP estático VBScript, na Galeria do TechNet, usa **EnableStatic** para definir o endereço IP de um computador.

O exemplo de VBScript a seguir demonstra como desabilitar o uso de DHCP em uma instância do [**\_ NetworkAdapterConfiguration do Win32.**](win32-networkadapterconfiguration.md) Nesse caso, especificamos o adaptador com um Índice de 0. O índice correto deve ser selecionado nas instâncias do Win32 \_ NetworkAdapter para outras interfaces.

> [!Note]  
> Esse script só se aplica a sistemas baseados em NT Altere as variáveis de ipaddr e sub-rede abaixo para os valores que você deseja aplicar ao adaptador.

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



O exemplo de Perl a seguir demonstra como desabilitar o uso de DHCP em uma instância do [**\_ NetworkAdapterConfiguration do Win32.**](win32-networkadapterconfiguration.md) Nesse caso, especificamos o adaptador com um Índice de 0. O índice correto deve ser selecionado nas instâncias do Win32 \_ NetworkAdapter para outras interfaces.

> [!Note]  
> Esse script só se aplica a sistemas baseados em NT Altere as variáveis de ipaddr e sub-rede abaixo para os valores que você deseja aplicar ao adaptador.

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
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

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Tarefas WMI: Rede](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tarefas WMI: contas e domínios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Suporte a IPv6 e IPv4 no WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

