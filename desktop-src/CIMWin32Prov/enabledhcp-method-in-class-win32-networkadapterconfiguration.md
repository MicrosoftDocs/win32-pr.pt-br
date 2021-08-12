---
description: O método de classe WMI EnableDHCP habilita o protocolo DHCP para serviço com esse adaptador de rede. O DHCP permite que os endereços IP sejam alocados dinamicamente.
ms.assetid: 8c61d731-77a3-4ef4-bad9-26edaca60892
ms.tgt_platform: multiple
title: Método EnableDHCP da classe Win32_NetworkAdapterConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDHCP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d5be73abab17303cce7a9a0e4ae2beab9bdb53df6a45d0162a575ce167ee1df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676572"
---
# <a name="enabledhcp-method-of-the-win32_networkadapterconfiguration-class"></a>Método EnableDHCP da classe \_ NetworkAdapterConfiguration do Win32

O método de classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableDHCP** habilita o protocolo DHCP para serviço com esse adaptador de rede. O DHCP permite que os endereços IP sejam alocados dinamicamente.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableDHCP();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

Não é possível configurar o serviço DHCP.

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

**Outras**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse método não limpa nenhum gateway padrão estático presente no computador.

## <a name="examples"></a>Exemplos

O [exemplo de código Habilitar DHCP](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) e Atribuir Servidores DNS VBScript na Galeria do TechNet usa EnableDHCP para habilitar o DHCP e atribuir servidores DNS a um computador.

O exemplo de código VBScript a seguir demonstra como habilitar o uso de DHCP em uma instância do [**\_ NetworkAdapterConfiguration do Win32.**](win32-networkadapterconfiguration.md) Nesse caso, especificamos o adaptador com um Índice de 0. O índice correto deve ser selecionado nas instâncias do Win32 \_ NetworkAdapter para outras interfaces.

> [!Note]  
> Com suporte apenas em plataformas NT.

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=0")

RetVal = Adapter.EnableDHCP()

if RetVal = 0 then 
 WScript.Echo "DHCP Enabled"
else 
 WScript.Echo "DHCP enable failed"
end if
```



O exemplo de código Perl a seguir demonstra como habilitar o uso de DHCP em uma instância do [**\_ NetworkAdapterConfiguration do Win32.**](win32-networkadapterconfiguration.md) Nesse caso, especificamos o adaptador com um Índice de 0. O índice correto deve ser selecionado nas instâncias do Win32 \_ NetworkAdapter para outras interfaces.

> [!Note]  
> Com suporte apenas em plataformas NT.

 


```
use strict;
use Win32::OLE;

my ( $Adapter, $RetVal );

eval { $Adapter = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
       Get("Win32_NetworkAdapterConfiguration=0"); };
unless ($@)
{
 print "\n";
 $RetVal = $Adapter->EnableDHCP();
 if ( $RetVal == 0)
 {
  print "DHCP Enabled\n";
 }
 else
 {
  print "DHCP enable failed\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
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



## <a name="see-also"></a>Consulte também

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

 

