---
title: Estrutura GUESTOSVERSIONINFOEX (VPCCOMInterfaces.h)
description: Contém informações de versão do sistema operacional para o sistema operacional convidado.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- PC Virtual da estrutura GUESTOSVERSIONINFOEX
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848196448c2bd6f021d85f7c13972e81664dd60a0e4a0bbbd2e05ef3455aade7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056904"
---
# <a name="guestosversioninfoex-structure"></a>Estrutura GUESTOSVERSIONINFOEX

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Contém informações de versão do sistema operacional para o sistema operacional convidado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwosversioninfosize**
</dt> <dd>

O tamanho dessa estrutura de dados, em bytes. De definir esse membro como `sizeof(GUESTOSVERSIONINFOEX)` .

</dd> <dt>

**dwMajorVersion**
</dt> <dd>

O número da versão principal.

</dd> <dt>

**dwMinorVersion**
</dt> <dd>

O número da versão secundária.

</dd> <dt>

**dwBuildNumber**
</dt> <dd>

O número de build.

</dd> <dt>

**dwPlatformId**
</dt> <dd>

A plataforma do sistema operacional. Esse membro pode ser **VER \_ PLATFORM \_ WIN32 \_ NT** (2).

</dd> <dt>

**szCSDVersion**
</dt> <dd>

Uma cadeia de caracteres terminada em nulo, como "Service Pack 3", que indica o Service Pack mais recente instalado no sistema. Se nenhum Service Pack tiver sido instalado, a cadeia de caracteres será vazia.

</dd> <dt>

**wServicePackMajor**
</dt> <dd>

O número de versão principal do Service Pack mais recente instalado.

</dd> <dt>

**wServicePackMinor**
</dt> <dd>

O número de versão secundária do Service Pack mais recente instalado.

</dd> <dt>

**wSuiteMask**
</dt> <dd>

Um bitmask que identifica os pacote de produtos disponíveis no sistema. Esse membro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**VER \_ PACOTE \_ BACKOFFICE**</dt> <dt>0X00000004</dt> </dl>                                            | Os componentes do Microsoft BackOffice estão instalados.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**VER \_ FOLHA \_ DO**</dt> <dt>PACOTE 0X00000400</dt> </dl>                                                           | Windows Server 2003, Web Edition está instalado.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**VER \_ PACOTE \_ DE SERVIDORES DE \_ COMPUTAÇÃO**</dt> <dt>0X00004000</dt> </dl>                               | Windows Server 2003, Edição de Cluster de Computação instalada.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**VER \_ PACOTE \_ DE DATACENTER**</dt> <dt>0X00000080</dt> </dl>                                            | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition ou Windows 2000 Datacenter Server está instalado.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**VER \_ SUITE \_ ENTERPRISE**</dt> <dt>0X00000002</dt> </dl>                                            | Windows Server 2008 Enterprise, Windows Server 2003, Edição Enterprise ou Windows 2000 Advanced Server está instalado. Consulte a seção Comentários para obter mais informações sobre esse sinalizador de bits.<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**VER \_ PACOTE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt> </dl>                                            | Windows O XP Embedded está instalado.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**VER \_ PACOTE \_ PESSOAL**</dt> <dt>0X00000200</dt> </dl>                                                  | Windows O Vista Home Premium, Windows Vista Home Basic ou Windows XP Home Edition está instalado.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**VER \_ PACOTE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt> </dl>                                      | Área de Trabalho Remota há suporte, mas há suporte para apenas uma sessão interativa. Esse valor é definido, a menos que o sistema esteja em execução no modo de servidor de aplicativos.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**VER \_ PACOTE \_ SMALLBUSINESS**</dt> <dt>0X00000001</dt> </dl>                                   | O Microsoft Small Business Server já foi instalado no sistema, mas pode ter sido atualizado para outra versão do Windows. Consulte a seção Comentários para obter mais informações sobre esse sinalizador de bits.<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**VER \_ SUITE \_ SMALLBUSINESS \_ RESTRICTED**</dt> <dt>0X00000020</dt> </dl> | O Microsoft Small Business Server é instalado com a licença de cliente restritiva em vigor. Consulte a seção Comentários para obter mais informações sobre esse sinalizador de bits.<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**VER \_ SERVIDOR \_ DE ARMAZENAMENTO DO \_**</dt> <dt>PACOTE 0X00002000</dt> </dl>                               | Windows Armazenamento Server 2003 R2 ou Windows Armazenamento Server 2003 está instalado.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**VER \_ PACOTE \_ TERMINAL**</dt> <dt>0X00000010</dt> </dl>                                                  | Os Serviços de Terminal estão instalados. Esse valor é sempre definido.<br/> Se **VER \_ SUITE \_ TERMINAL** estiver definido, **mas VER SUITE \_ \_ SINGLEUSERTS** não estiver definido, o sistema será executado no modo de servidor de aplicativos.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**VER \_ SUITE \_ WH \_ SERVER**</dt> <dt>0x00008000</dt> </dl>                                              | Windows O Home Server está instalado.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

Quaisquer informações adicionais sobre o sistema. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**VER \_ CONTROLADOR DE DOMÍNIO NT \_ \_ 0x0000002**</dt> <dt></dt> </dl> | O sistema é um controlador de domínio e o sistema operacional é Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**VER \_ NT \_ SERVER**</dt> <dt>0x0000003</dt> </dl>                                   | O sistema operacional é Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.<br/> Observe que um servidor que também é um controlador de domínio é relatado como **VER \_ NT \_ DOMAIN \_ CONTROLLER,** não **VER \_ NT \_ SERVER.**<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**VER \_ NT \_ WORKSTATION**</dt> <dt>0x0000001</dt> </dl>                    | O sistema operacional é Windows 7, Windows Vista, Windows XP ou Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS::GetOsVersionInfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

