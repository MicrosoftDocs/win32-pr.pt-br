---
description: O método de classe WMI SetWINSServer define os servidores WINS (Windows Internet Serviço de Nomenclatura) primários e secundários neste adaptador de rede associado a TCP/IP. Esse método é aplicado independentemente do adaptador de rede.
ms.assetid: fa8ce436-b67e-4975-a5c5-1a7d6aab4c8e
ms.tgt_platform: multiple
title: Método SetWINSServer da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetWINSServer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49bfb0103a7d9cbbd6ea3faa0e1a868bac7b0196
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751800"
---
# <a name="setwinsserver-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetWINSServer da classe Win32 \_ NetworkAdapterConfiguration

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetWINSServer** define os servidores WINS (Windows Internet serviço de nomenclatura) primários e secundários neste adaptador de rede associado a TCP/IP. Esse método é aplicado independentemente do adaptador de rede.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetWINSServer(
  [in] string WINSPrimaryServer,
  [in] string WINSSecondaryServer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*WINSPrimaryServer* \[ no\]
</dt> <dd>

Endereço IP do servidor WINS primário.

> [!Note]  
> Sempre verifique a validade desse endereço IP quando ele for de uma fonte desconhecida ou uma fonte na qual você não confia.

 

</dd> <dt>

*WINSSecondaryServer* \[ no\]
</dt> <dd>

Endereço IP do servidor WINS secundário.

> [!Note]  
> Sempre verifique a validade desse endereço IP quando ele for de uma fonte desconhecida ou uma fonte na qual você não confia.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor inteiro de 0 (zero) após a conclusão bem-sucedida e qualquer outro número para indicar um erro. Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

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

Não é possível configurar o serviço DHCP.

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

**Outras**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

Se *WINSPrimaryServer* e *WINSSecondaryServer* forem definidos como "" (uma cadeia de caracteres vazia), os servidores WINS explícitos voltarão ao DHCP.

## <a name="examples"></a>Exemplos

[O atribuir um endereço IP recuperado de um banco de dados](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) Exemplo de código VBScript pesquisa um computador em um banco de dados e atribui esse computador ao endereço IP especificado.

O exemplo de código VBScript a seguir define o servidor WINS primário e secundário para um adaptador de rede associado a TCP/IP.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    strPrimaryServer = "192.168.1.100" 
    strSecondaryServer = "192.168.1.200" 
    objNetCard.SetWINSServer strPrimaryServer, strSecondaryServer 
Next 
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

 

