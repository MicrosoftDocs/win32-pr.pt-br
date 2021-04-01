---
description: O método de classe WMI EnableStatic permite endereçamento TCP/IP estático para o adaptador de rede de destino. Como resultado, o DHCP para esse adaptador de rede está desabilitado.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Método EnableStatic da classe Win32_NetworkAdapterConfiguration
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
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646310"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a>Método EnableStatic da classe Win32 \_ NetworkAdapterConfiguration

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableStatic** permite endereçamento TCP/IP estático para o adaptador de rede de destino. Como resultado, o DHCP para esse adaptador de rede está desabilitado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IPAddress* \[ no\]
</dt> <dd>

Lista todos os endereços IP estáticos para o adaptador de rede atual.

Exemplo: 155.34.22.0.

</dd> <dt>

*Submáscara de rede* \[ no\]
</dt> <dd>

Máscaras de sub-rede que complementam os valores no parâmetro *IPAddress* .

Exemplo: 255.255.0.0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro número se houver um erro. Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida, nenhuma reinicialização necessária**
</dt> <dd>

0

Conclusão bem-sucedida, nenhuma reinicialização necessária.

</dd> <dt>

**Conclusão bem-sucedida, reinicialização necessária**
</dt> <dd>

1

Conclusão bem-sucedida, reinicialização necessária.

</dd> <dt>

**Método sem suporte nesta plataforma**
</dt> <dd>

64

Método sem suporte nesta plataforma.

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

**Ocorreu um erro ao processar uma instância que foi retornada**
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

**Endereço IP de gateway inválido**
</dt> <dd>

71

Endereço IP do gateway inválido.

</dd> <dt>

**Ocorreu um erro ao acessar o registro para as informações solicitadas**
</dt> <dd>

72

Ocorreu um erro ao acessar o registro para obter as informações solicitadas.

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

**Caminho de sistema inválido**
</dt> <dd>

77

Caminho de sistema inválido.

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

**Não é possível renovar a concessão DHCP**
</dt> <dd>

82

Não é possível renovar a concessão DHCP.

</dd> <dt>

**Não é possível liberar a concessão DHCP**
</dt> <dd>

83

Não é possível liberar a concessão DHCP.

</dd> <dt>

**IP não habilitado no adaptador**
</dt> <dd>

84

O IP não está habilitado no adaptador.

</dd> <dt>

**IPX não habilitado no adaptador**
</dt> <dd>

85

IPX não habilitado no adaptador.

</dd> <dt>

**Erro de limites de número de quadro/rede**
</dt> <dd>

86

Erro de limites de número de rede ou quadro.

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

Acesso negado.

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

**Nem todas as concessões DHCP puderam ser liberadas/renovadas**
</dt> <dd>

98

Nem todas as concessões DHCP podem ser liberadas ou renovadas.

</dd> <dt>

**DHCP não habilitado no adaptador**
</dt> <dd>

100

DHCP não habilitado no adaptador.

</dd> <dt>

**2147786788**
</dt> <dd>

Bloqueio de gravação não habilitado. Para obter mais informações, consulte [**INetCfgLock:: AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).

</dd> <dt>

**Outras**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao usar o **EnableStatic** para alterar o endereço IP do computador remoto, ao ser conectado por meio desse adaptador, você provavelmente perderá a conexão com o computador remoto e receberá uma mensagem de erro de RPC não disponível. (no entanto, as configurações são alteradas). Para evitar esse cenário, considere alterar o gateway e/ou as configurações de DNS antes de definir o endereço IP do adaptador.

Ao usar **EnableStatic** para dar um adaptador a uma configuração de IP estático, a função retorna um "81-não é possível configurar o serviço DHCP" se o adaptador já estiver configurado com um endereço estático. No entanto, a função ainda terá sucesso na configuração com a nova operação.

## <a name="examples"></a>Exemplos

O [IP estático e, em seguida, ingressar em um](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) exemplo de código do PowerShell de domínio, na galeria do TechNet, usa **EnableStatic** para adicionar um IP estático a um computador local.

O exemplo de código do VBScript [atribuir um endereço IP estático](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) , na galeria do TechNet, usa **EnableStatic** para definir o endereço IP de um computador.

O exemplo de VBScript a seguir demonstra como desabilitar o uso do DHCP em uma instância do [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md). Nesse caso, especificamos o adaptador com um índice de 0. O índice correto deve ser selecionado em instâncias do Win32 \_ adaptador para outras interfaces.

> [!Note]  
> Esse script se aplica somente a sistemas baseados em NT altere as IPADDR e as variáveis de sub-rede abaixo para os valores que você deseja aplicar ao adaptador.

 


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



O exemplo do Perl a seguir demonstra como desabilitar o uso do DHCP em uma instância do [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md). Nesse caso, especificamos o adaptador com um índice de 0. O índice correto deve ser selecionado em instâncias do Win32 \_ adaptador para outras interfaces.

> [!Note]  
> Esse script se aplica somente a sistemas baseados em NT altere as IPADDR e as variáveis de sub-rede abaixo para os valores que você deseja aplicar ao adaptador.

 


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
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Tarefas do WMI: rede](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tarefas do WMI: contas e domínios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Suporte a IPv6 e IPv4 no WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

