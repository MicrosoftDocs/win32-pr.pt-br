---
title: Estrutura GUESTOSVERSIONINFOEX (VPCCOMInterfaces. h)
description: Contém informações de versão do sistema operacional para o sistema operacional convidado.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- Virtual PC de estrutura GUESTOSVERSIONINFOEX
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
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085755"
---
# <a name="guestosversioninfoex-structure"></a>Estrutura GUESTOSVERSIONINFOEX

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

**dwOSVersionInfoSize**
</dt> <dd>

O tamanho dessa estrutura de dados, em bytes. Defina este membro como `sizeof(GUESTOSVERSIONINFOEX)` .

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

A plataforma do sistema operacional. Esse membro pode ser **ver a \_ plataforma \_ Win32 \_ NT** (2).

</dd> <dt>

**szCSDVersion**
</dt> <dd>

Uma cadeia de caracteres terminada em nulo, como "Service Pack 3", que indica o Service Pack mais recente instalado no sistema. Se nenhum Service Pack tiver sido instalado, a cadeia de caracteres estará vazia.

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

Um bitmask que identifica os pacotes de produtos disponíveis no sistema. Esse membro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**Ver \_ PACOTE de \_ backoffice**</dt> <dt>0x00000004</dt> </dl>                                            | Os componentes do Microsoft BackOffice são instalados.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**Ver \_ 0x00000400 \_ Blade Suite**</dt> <dt></dt> </dl>                                                           | O Windows Server 2003, Web Edition está instalado.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**Ver \_ Pacote de \_ computação \_ do Suite**</dt> <dt>0x00004000</dt> </dl>                               | O Windows Server 2003, Compute Cluster Edition, está instalado.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**Ver \_ 0x00000080 do \_ DATAcenter do pacote**</dt> <dt></dt> </dl>                                            | O Windows Server 2008 Datacenter, o Windows Server 2003, o Datacenter Edition ou o Windows 2000 Datacenter Server está instalado.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**Ver \_ SUITE \_ Enterprise**</dt> <dt>0x00000002</dt> </dl>                                            | O Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server está instalado. Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**Ver \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt> </dl>                                            | O Windows XP Embedded está instalado.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**Ver \_ 0x00000200 \_ pessoal de Suite**</dt> <dt></dt> </dl>                                                  | O Windows Vista Home Premium, o Windows Vista Home Basic ou o Windows XP Home Edition está instalado.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**Ver \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt> </dl>                                      | Há suporte para Área de Trabalho Remota, mas há suporte para apenas uma sessão interativa. Esse valor é definido, a menos que o sistema esteja sendo executado no modo de servidor de aplicativos.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**Ver \_ PACOTE do \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt> </dl>                                   | O Microsoft Small Business Server já foi instalado no sistema, mas pode ter sido atualizado para outra versão do Windows. Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**Ver \_ CONJUNTO de o do \_ SMALLBUSINESS \_ Restricted**</dt> <dt>0x00000020</dt> </dl> | O Microsoft Small Business Server é instalado com a licença de cliente restritiva em vigor. Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**Ver \_ CONJUNTO de 0x00002000 \_ \_ do servidor de armazenamento**</dt> <dt></dt> </dl>                               | O Windows Storage Server 2003 R2 ou o Windows Storage Server 2003 está instalado.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**Ver \_ \_Terminal do Suite**</dt> <dt>0x00000010</dt> </dl>                                                  | Os serviços de terminal estão instalados. Esse valor é sempre definido.<br/> Se **o \_ \_ terminal Suite ver** estiver definido, mas o **\_ \_ SINGLEUSERTS Suite** não estiver definido, o sistema estará sendo executado no modo de servidor de aplicativos.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**Ver \_ 0x00008000 \_ \_ do servidor do Suite**</dt> <dt></dt> </dl>                                              | O Windows Home Server está instalado.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

Quaisquer informações adicionais sobre o sistema. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**Ver \_ 0x0000002 \_ do \_ controlador de domínio NT**</dt> <dt></dt> </dl> | O sistema é um controlador de domínio e o sistema operacional é o Windows Server 2008 R2, o Windows Server 2008, o Windows Server 2003 R2, o Windows Server 2003 ou o Windows 2000 Server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**Ver \_ 0x0000003 NT \_ Server**</dt> <dt></dt> </dl>                                   | O sistema operacional é o Windows Server 2008 R2, o Windows Server 2008, o Windows Server 2003 R2, o Windows Server 2003 ou o Windows 2000 Server.<br/> Observe que um servidor que também é um controlador de domínio é relatado **como \_ \_ \_ controlador de domínio do NT**, não ver o **\_ \_ servidor NT**.<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**Ver \_ NT \_ Workstation**</dt> <dt>0x0000001</dt> </dl>                    | O sistema operacional é o Windows 7, o Windows Vista, o Windows XP ou o Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS::GetOsVersionInfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

