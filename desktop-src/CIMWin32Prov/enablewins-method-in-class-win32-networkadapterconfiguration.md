---
description: EnableWINS ativa &\# 32; O método estático da classe WMI habilita as configurações do Windows Internet Serviço de Nomenclatura (WINS) específicas para TCP/IP, mas independente do adaptador de rede.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Método EnableWINS ativa da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500884"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>Método EnableWINS ativa da classe Win32 \_ NetworkAdapterConfiguration

O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS ativa** habilita as configurações WINS (Windows Internet serviço de nomenclatura) específicas para TCP/IP, mas independente do adaptador de rede.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DNSEnabledForWINSResolution* \[ no\]
</dt> <dd>

Se for **true**, o DNS (sistema de nomes de domínio) será habilitado para resolução de nomes sobre a resolução WINS.

</dd> <dt>

*WINSEnableLMHostsLookup* \[ no\]
</dt> <dd>

Se **for true**, os arquivos de pesquisa local serão usados. Arquivos de pesquisa conterão mapeamentos de endereços IP para nomes de host.

</dd> <dt>

*WINSHostLookupFile* \[ em, opcional\]
</dt> <dd>

Arquivos de pesquisa que contêm mapeamentos de endereços IP para nomes de host. Se disponível, os arquivos serão encontrados nos drivers% SystemRoot% \\ System32 \\ \\ .

</dd> <dt>

*WINSScopeID* \[ em, opcional\]
</dt> <dd>

O valor do identificador de escopo que será anexado ao final do nome NetBIOS do computador. Os sistemas que usam o mesmo identificador de escopo podem se comunicar com este computador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária; 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária; um número diferente se houver um erro. Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida, nenhuma reinicialização necessária** (0)
</dt> <dt>

**Conclusão bem-sucedida, reinicialização necessária** (1)
</dt> <dt>

**Método sem suporte nesta plataforma** (64)
</dt> <dt>

**Falha desconhecida** (65)
</dt> <dt>

**Máscara de sub-rede inválida** (66)
</dt> <dt>

**Ocorreu um erro ao processar uma instância que foi retornada** (67)
</dt> <dt>

**Parâmetro de entrada inválido** (68)
</dt> <dt>

**Mais de 5 gateways especificados** (69)
</dt> <dt>

**Endereço IP inválido** (70)
</dt> <dt>

**Endereço IP de gateway inválido** (71)
</dt> <dt>

**Ocorreu um erro ao acessar o registro para as informações solicitadas** (72)
</dt> <dt>

**Nome de domínio inválido** (73)
</dt> <dt>

**Nome de host inválido** (74)
</dt> <dt>

**Nenhum servidor WINS primário/secundário definido** (75)
</dt> <dt>

**Arquivo inválido** (76)
</dt> <dt>

**Caminho de sistema inválido** (77)
</dt> <dt>

**Falha na cópia do arquivo** (78)
</dt> <dt>

**Parâmetro de segurança inválido** (79)
</dt> <dt>

**Não é possível configurar o serviço TCP/IP** (80)
</dt> <dt>

**Não é possível configurar o serviço DHCP** (81)
</dt> <dt>

**Não é possível renovar a concessão DHCP** (82)
</dt> <dt>

**Não é possível liberar a concessão DHCP** (83)
</dt> <dt>

**IP não habilitado no adaptador** (84)
</dt> <dt>

**IPX não habilitado no adaptador** (85)
</dt> <dt>

**Erro de limites de número de quadro/rede** (86)
</dt> <dt>

**Tipo de quadro inválido** (87)
</dt> <dt>

**Número de rede inválido** (88)
</dt> <dt>

**Número de rede duplicado** (89)
</dt> <dt>

**Parâmetro fora dos limites** (90)
</dt> <dt>

**Acesso negado** (91)
</dt> <dt>

**Memória insuficiente** (92)
</dt> <dt>

**Já existe** (93)
</dt> <dt>

**Caminho, arquivo ou objeto não encontrado** (94)
</dt> <dt>

**Não é possível notificar o serviço** (95)
</dt> <dt>

**Não é possível notificar o serviço DNS** (96)
</dt> <dt>

**Interface não configurável** (97)
</dt> <dt>

**Nem todas as concessões DHCP puderam ser liberadas/renovadas** (98)
</dt> <dt>

**DHCP não habilitado no adaptador** (100)
</dt> <dt>

**Outro** (101 4294967295)
</dt> </dl>

## <a name="examples"></a>Exemplos

O exemplo de código [Ativar WINS para todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript, na galeria do TechNet, usa **EnableWINS ativa** para habilitar o WINS em todos os adaptadores de rede instalados em um computador.

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

 

