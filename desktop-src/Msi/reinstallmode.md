---
description: A propriedade REINSTALLMODE é uma cadeia de caracteres que contém letras especificando o tipo de reinstalação a ser executado.
ms.assetid: 756d2899-2cfe-473a-bebf-a7f7bbe7d229
title: Propriedade REINSTALLMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 227a069fa0974758bf623c83ef23d40902d9feb140f69446c57c2d723468054f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637870"
---
# <a name="reinstallmode-property"></a>Propriedade REINSTALLMODE

A propriedade **REinstallmode** é uma cadeia de caracteres que contém letras especificando o tipo de reinstalação a ser executado. As opções não diferenciam maiúsculas de minúsculas e independentes de ordem. Essa propriedade normalmente deve ser sempre usada em conjunto com a propriedade [**REINSTALL**](reinstall.md) . No entanto, essa propriedade também pode ser usada durante a instalação, não apenas reinstalar.

> [!Note]  
> o Windows Installer ignora a propriedade **reinstallmode** durante uma [instalação administrativa](administrative-installation.md).

 

## <a name="reinstall-option-codes"></a>Reinstalar códigos de opção

Por padrão, o **REinstallmode** é "omus".



| Código | Opção                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| p    | Reinstale somente se o arquivo estiver ausente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| o    | Reinstale se o arquivo estiver ausente ou se for uma versão mais antiga.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| e    | Reinstale se o arquivo estiver ausente ou se for uma versão igual ou anterior.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| d    | Reinstale se o arquivo estiver ausente ou se uma versão diferente estiver presente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| c    | Verifique os valores da soma de verificação e reinstale o arquivo se eles estiverem ausentes ou corrompidos. Esse sinalizador repara apenas os arquivos que têm msidbFileAttributesChecksum na coluna atributos da [tabela de arquivos](file-table.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| um    | Forçar todos os arquivos a serem reinstalados, independentemente da soma de verificação ou da versão.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| u    | Reescreva todas as entradas de Registro necessárias da [tabela de registro](registry-table.md) que vão para o **\_ \_ usuário atual do hKey**<br/> ou o **HKEY \_ Users**<br/> hive do registro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| m    | Reescreva todas as entradas de Registro necessárias da [tabela de registro](registry-table.md) que vão para o **\_ \_ computador local hKey**<br/> ou **HKEY \_ classes \_ root**<br/> hive do registro. Reescreva todas as informações da [tabela de classes](class-table.md), da [tabela de verbos](verb-table.md), da [tabela PublishComponent](publishcomponent-table.md), da tabela [ProgID](progid-table.md), da tabela [MIME](mime-table.md), da tabela de [ícones](icon-table.md), da [tabela de extensões](extension-table.md)e da [tabela AppID](appid-table.md) , independentemente da atribuição do computador ou do usuário. Reinstale todos os [**componentes qualificados.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) Ao reinstalar um aplicativo, essa opção executa as ações [RegisterTypeLibraries](registertypelibraries-action.md) e [InstallODBC](installodbc-action.md) .<br/> |
| s    | Reinstale todos os atalhos e armazene novamente em cache todos os ícones, substituindo quaisquer atalhos e ícones existentes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| v    | Use para executar a partir do pacote de origem e armazenar em cache novamente o pacote local. Não use o código de opção v REINSTALL para a primeira instalação de um aplicativo ou recurso.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

Se a propriedade **REinstallmode** for definida sem também definir a propriedade [**REINSTALL**](reinstall.md) , os modos de "detecção" especificados ainda serão aplicados e especificarão o modo de "substituição" para uma instalação normal. A propriedade **REinstallmode** afeta apenas os recursos que são selecionados normalmente para instalação. A presença da propriedade **REinstallmode** não reinstala recursos. A reinstalação de recursos requer a presença da propriedade **reinstalar** .

Os códigos de opção para essa propriedade correspondem à [opção de linha de comando](command-line-options.md) '/f '. A opção de linha de comando tem um valor padrão de ' pecms '.

> [!Note]  
> Somente os arquivos que contêm informações de soma de verificação já são verificados e reparados. O sinalizador fileverify de reinstalaçãomode \_ (o ccode acima) repara apenas os arquivos que têm msidbFileAttributesChecksum na coluna atributos da [tabela de arquivos](file-table.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




