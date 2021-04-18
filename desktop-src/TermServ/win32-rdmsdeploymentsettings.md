---
title: Classe Win32_RDMSDeploymentSettings
description: Gerencia configurações de implantação para uma coleção de áreas de trabalho virtuais.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSDeploymentSettings classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499323"
---
# <a name="win32_rdmsdeploymentsettings-class"></a>\_Classe Win32 RDMSDeploymentSettings

Gerencia configurações de implantação para uma coleção de áreas de trabalho virtuais.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RDMSDeploymentSettings** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RDMSDeploymentSettings** tem esses métodos.



| Método                                                                                                  | Descrição                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBaseVHDPath**](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Recupera o caminho base para o diretório no qual os VHDs do conjunto de áreas de trabalho virtuais são implantados.<br/>                 |
| [**GetConnectionString**](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | Recupera a cadeia de conexão do banco de dados de nível de implantação.<br/>                                                             |
| [**GetDiffVHDPath**](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Recupera o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.<br/>            |
| [**GetExportPath**](getexportpath-win32-rdmsdeploymentsettings.md)                                     | Recupera o caminho do diretório para o qual as máquinas virtuais são implantadas para uma coleção de áreas de trabalho virtuais.<br/>                  |
| [**Getint32property**](getint32property-win32-rdmsdeploymentsettings.md)                               | Recupera uma propriedade de número inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.<br/>                             |
| [**GetSecondaryConnectionString**](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | Recupera a cadeia de conexão secundária do banco de dados no nível da implantação, que pode ser usada para dar suporte à expiração da senha.<br/> |
| [**GetSMBPath**](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | Recupera o caminho UNC para o compartilhamento SMB no qual as máquinas virtuais do conjunto de áreas de trabalho virtuais são implantadas.<br/>      |
| [**GetStringArrayDeploymentSetting**](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Recupera as configurações de implantação para uma coleção de áreas de trabalho virtuais.<br/>                                                    |
| [**Getstringproperty**](getstringproperty-win32-rdmsdeploymentsettings.md)                             | Recupera uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.<br/>                               |
| [**RemoveDeploymentSetting**](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | Exclui as configurações de implantação para uma coleção de áreas de trabalho virtuais.<br/>                                                      |
| [**SetBaseVHDPath**](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Recupera o caminho base para o diretório no qual os VHDs do conjunto de áreas de trabalho virtuais são implantados.<br/>                 |
| [**SetConnectionString**](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | Define a cadeia de conexão do banco de dados de nível de implantação.<br/>                                                                  |
| [**SetDiffVHDPath**](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Atualiza o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.<br/>              |
| [**SetExportPath**](setexportpath-win32-rdmsdeploymentsettings.md)                                     | Atualiza o caminho do diretório para o qual as máquinas virtuais são implantadas para uma coleção de áreas de trabalho virtuais.<br/>                    |
| [**Setint32property**](setint32property-win32-rdmsdeploymentsettings.md)                               | Atualiza uma propriedade de inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.<br/>                               |
| [**SetSecondaryConnectionString**](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | Define a cadeia de conexão secundária do banco de dados no nível da implantação.<br/>                                                        |
| [**SetSMBPath**](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | Atualiza o caminho UNC para o compartilhamento SMB no qual as máquinas virtuais do conjunto de áreas de trabalho virtuais são implantadas.<br/>        |
| [**SetStringArrayDeploymentSetting**](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Atualiza as configurações de implantação para uma coleção de áreas de trabalho virtuais.<br/>                                                      |
| [**Setstringproperty**](setstringproperty-win32-rdmsdeploymentsettings.md)                             | Atualiza uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.<br/>                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor de serviços de gerenciamento de Área de Trabalho Remota](rdms-api-reference.md)
</dt> </dl>

 

 





