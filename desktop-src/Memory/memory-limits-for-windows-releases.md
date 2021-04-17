---
description: Este tópico descreve os limites de memória para versões do Windows e do Windows Server com suporte.
ms.assetid: de09c8af-0ed8-4fd4-b8e8-2c921aafe6f2
title: Limites de memória para as versões do Windows e do Windows Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09db7d303468247794807629d3a56e786c4ada6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812764"
---
# <a name="memory-limits-for-windows-and-windows-server-releases"></a>Limites de memória para as versões do Windows e do Windows Server

Este tópico descreve os limites de memória para versões do Windows e do Windows Server com suporte.

-   [Limites de espaço de endereço e memória](#memory-limits-for-windows-and-windows-server-releases)
-   [Limites de memória física: Windows 10](#physical-memory-limits-windows-10)
-   [Limites de memória física: Windows Server 2016](#physical-memory-limits-windows-server-2016)
-   [Limites de memória física: Windows 8](#physical-memory-limits-windows-8)
-   [Limites de memória física: Windows Server 2012](#physical-memory-limits-windows-server-2012)
-   [Limites de memória física: Windows 7](#physical-memory-limits-windows-7)
-   [Limites de memória física: Windows Server 2008 R2](#physical-memory-limits-windows-server-2008-r2)
-   [Limites de memória física: Windows Server 2008](#physical-memory-limits-windows-server-2008-r2)
-   [Limites de memória física: Windows Vista](#physical-memory-limits-windows-vista)
-   [Limites de memória física: Windows Home Server](#physical-memory-limits-windows-home-server)
-   [Limites de memória física: Windows Server 2003 R2](#physical-memory-limits-windows-server-2003-r2)
-   [Limites de memória física: Windows Server 2003 com Service Pack 2 (SP2)](#physical-memory-limits-windows-server-2003-with-service-pack-2-sp2)
-   [Limites de memória física: Windows Server 2003 com Service Pack 1 (SP1)](#physical-memory-limits-windows-server-2003-with-service-pack-1-sp1)
-   [Limites de memória física: Windows Server 2003](#physical-memory-limits-windows-server-2003-r2)
-   [Limites de memória física: Windows XP](#physical-memory-limits-windows-xp)
-   [Limites de memória física: Windows Embedded](#physical-memory-limits-windows-embedded)
-   [Como placas gráficas e outros dispositivos afetam os limites de memória](#how-graphics-cards-and-other-devices-affect-memory-limits)
-   [Tópicos relacionados](#related-topics)

Os limites de memória e espaço de endereço variam por plataforma, sistema operacional e por se o valor de **\_ \_ \_ \_ reconhecimento de endereço grande do arquivo de imagem** da estrutura de [**\_ imagem carregada**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) e o [ajuste de 4 gigabytes](4-gigabyte-tuning.md) (4GT) estão em uso. **Imagem \_ do O \_ \_ \_ reconhecimento de endereço grande de arquivo** é definido ou limpo usando a opção de vinculador [/LARGEADDRESSAWARE](/cpp/build/reference/largeaddressaware-handle-large-addresses?view=vs-2019) .

o ajuste de 4 gigabytes (4GT), também conhecido como ajuste de memória de aplicativo, ou a opção/3GB, é uma tecnologia (aplicável somente a sistemas de 32 bits) que altera a quantidade de espaço de endereço virtual disponível para aplicativos de modo de usuário. A habilitação dessa tecnologia reduz o tamanho geral do espaço de endereço virtual do sistema e, portanto, os máximos de recursos do sistema. Para obter mais informações, consulte [o que é 4GT]( /previous-versions/windows/it-pro/windows-server-2003/cc786709(v=ws.10)).

Os limites de memória física para plataformas de 32 bits também dependem da [extensão de endereço físico](physical-address-extension.md) (PAE), que permite que os sistemas Windows de 32 bits usem mais de 4 GB de memória física.

## <a name="memory-and-address-space-limits"></a>Limites de espaço de endereço e memória

A tabela a seguir especifica os limites de memória e espaço de endereço para as versões com suporte do Windows. Salvo indicação em contrário, os limites nesta tabela se aplicam a todas as versões com suporte.



| Tipo de memória                                                                                   | Limite em x86                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Limite no Windows de 64 bits                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Espaço de endereço virtual do modo de usuário para cada processo de 32 bits<br/>                            | 2 GB<br/> Até 3 GB com **reconhecimento de \_ \_ \_ endereço \_ grande de arquivo de imagem** e 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2 GB com **\_ reconhecimento de \_ \_ endereço grande \_ de arquivo de imagem** limpo (padrão)<br/> 4 GB com o conjunto de **\_ \_ \_ \_ reconhecimento de endereço grande do arquivo de imagem**<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Espaço de endereço virtual do modo de usuário para cada processo de 64 bits<br/>                            | Não aplicável<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Com imagem \_ Conjunto \_ de \_ \_ reconhecimento de endereço grande do arquivo** (padrão):<br/> **x64: Windows 8.1 e Windows Server 2012 R2 ou posterior:** 128 TB<br/> **x64: Windows 8 e Windows Server 2012 ou anterior** 8 TB<br/> **Sistemas Intel baseados em Itanium:** 7 TB<br/> <br/> 2 GB com **\_ reconhecimento de \_ \_ endereço grande \_ de arquivo de imagem** limpo<br/>                                                                                                                                                                                              |
| Espaço de endereço virtual no modo kernel<br/>                                                  | 2 GB<br/> De 1 GB até um máximo de 2 GB com 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Windows 8.1 e Windows Server 2012 R2 ou posterior:** 128 TB<br/> **Windows 8 e Windows Server 2012 ou anterior** 8 TB <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Pool Paginável<br/>                                                                         | 384 GB ou limite de confirmação do sistema, o que for menor. **Windows 8.1 e Windows Server 2012 R2:** 15,5 TB ou limite de confirmação do sistema, o que for menor. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Limitado pelo espaço de endereço virtual disponível no modo kernel. A partir do Windows Vista com Service Pack 1 (SP1), o pool paginável também pode ser limitado pelo valor da chave do registro [PagedPoolLimit](memory-management-registry-keys.md) .<br/> **Windows Home Server e Windows server 2003:** 530 MB<br/> **Windows XP:** 490 MB<br/> <br/>                                                                                                 | 384 GB ou limite de confirmação do sistema, o que for menor **Windows 8.1 e o Windows Server 2012 R2:** 15,5 TB ou limite de confirmação do sistema, o que for menor. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** 128 GB ou limite de confirmação do sistema, o que for menor<br/> **Windows Server 2003 e Windows XP:** Até 128 GB, dependendo da configuração e da RAM.<br/> <br/>                                                                                |
| Pool não paginável<br/>                                                                      | 75% de RAM ou 2 GB, o que for menor. **Windows 8.1 e Windows Server 2012 R2:** RAM ou 16 TB, o que for menor (o espaço de endereço é limitado a 2 x RAM).<br/> **Windows Vista:** Limitado apenas pelo espaço de endereço virtual do modo kernel e pela memória física. A partir do Windows Vista com SP1, o pool não paginável também pode ser limitado pelo valor da chave do registro [NonPagedPoolLimit](memory-management-registry-keys.md) .<br/> **Windows Home Server, Windows server 2003 e Windows XP:** 256 mb ou 128 MB com 4GT.<br/> <br/>                                                                                                                                                 | RAM ou 128 GB, o que for menor (o espaço de endereço é limitado a 2 x RAM) **Windows 8.1 e Windows Server 2012 R2:** RAM ou 16 TB, o que for menor (o espaço de endereço é limitado a 2 x RAM).<br/> **Windows server 2008 R2, Windows 7 e Windows server 2008:** 75% de RAM até um máximo de 128 GB<br/> **Windows Vista:** 40% de RAM até um máximo de 128 GB.<br/> **Windows Server 2003 e Windows XP:** Até 128 GB, dependendo da configuração e da RAM.<br/> <br/> |
| Espaço de endereço virtual do cache do sistema (tamanho físico limitado apenas pela memória física)<br/> | Limitado pelo espaço de endereço virtual do modo kernel disponível ou pelo valor da chave do registro [SystemCacheLimit](memory-management-registry-keys.md) .<br/> **Windows 8.1 e Windows Server 2012 R2:** 16 TB.<br/> **Windows Vista:** Limitado apenas pelo espaço de endereço virtual do modo kernel. A partir do Windows Vista com SP1, o espaço de endereço virtual de cache do sistema também pode ser limitado pelo valor da chave do registro [SystemCacheLimit](memory-management-registry-keys.md) .<br/> **Windows Home Server, Windows server 2003 e Windows XP:** 860 MB com o conjunto de chaves do registro [LARGESYSTEMCACHE](/previous-versions/windows/it-pro/windows-server-2003/cc784562(v=ws.10)) e sem 4GT; até 448 MB com 4GT.<br/> <br/> | Sempre 1 TB, independentemente da RAM física **Windows 8.1 e do Windows Server 2012 R2:** 16 TB.<br/> **Windows Server 2003 e Windows XP:** Até 1 TB, dependendo da configuração e da RAM.<br/> <br/>                                                                                                                                                                                                                                                                                            |



 

## <a name="physical-memory-limits-windows-10"></a>Limites de memória física: Windows 10

A tabela a seguir especifica os limites de memória física para o Windows 10.



| Versão               | Limite em x86    | Limite em x64     |
|-----------------------|-----------------|------------------|
| Windows 10 Enterprise | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Education  | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Pro for Workstations  | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Pro        | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Home       | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2016"></a>Limites de memória física: Windows Server 2016

A tabela a seguir especifica os limites de memória física para o Windows Server 2016.



| Versão                        | Limite em x64     |
|--------------------------------|------------------|
| Windows Server 2016 Datacenter | 24 TB<br/> |
| Windows Server 2016 Standard   | 24 TB<br/> |



 

## <a name="physical-memory-limits-windows-8"></a>Limites de memória física: Windows 8

A tabela a seguir especifica os limites de memória física para o Windows 8.



| Versão                | Limite em x86    | Limite em x64      |
|------------------------|-----------------|-------------------|
| O Windows 8 Enterprise   | 4 GB<br/> | 512 GB<br/> |
| Windows 8 Professional | 4 GB<br/> | 512 GB<br/> |
| Windows 8              | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2012"></a>Limites de memória física: Windows Server 2012

A tabela a seguir especifica os limites de memória física para o Windows Server 2012. O Windows Server 2012 está disponível apenas nas edições x64.



| Versão                               | Limite em x64     |
|---------------------------------------|------------------|
| Windows Server 2012 Datacenter        | 4 TB<br/>  |
| Windows Server 2012 Standard          | 4 TB<br/>  |
| Windows Server 2012 Essentials        | 64 GB<br/> |
| Windows Server 2012 Foundation        | 32 GB<br/> |
| Grupo de trabalho do Windows Storage Server 2012 | 32 GB<br/> |
| Windows Storage Server 2012 Standard  | 4 TB<br/>  |
| Hyper-V Server 2012                   | 4 TB<br/>  |



 

## <a name="physical-memory-limits-windows-7"></a>Limites de memória física: Windows 7

A tabela a seguir especifica os limites de memória física para o Windows 7.



| Versão                | Limite em x86    | Limite em x64      |
|------------------------|-----------------|-------------------|
| Windows 7 Ultimate     | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Enterprise   | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Professional | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows 7 Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows 7 Starter      | 2 GB<br/> | N/D<br/>    |



 

## <a name="physical-memory-limits-windows-server-2008-r2"></a>Limites de memória física: Windows Server 2008 R2

A tabela a seguir especifica os limites de memória física para o Windows Server 2008 R2. O Windows Server 2008 R2 está disponível apenas em edições de 64 bits.



| Versão                                          | Limite em x64      | Limite em IA64   |
|--------------------------------------------------|-------------------|-----------------|
| Windows Server 2008 R2 Datacenter                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 Enterprise                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 for Itanium-Based Systems |                   | 2 TB<br/> |
| Windows Server 2008 R2 Foundation                | 8 GB<br/>   |                 |
| Windows Server 2008 R2 Standard                  | 32 GB<br/>  |                 |
| Windows HPC Server 2008 R2                       | 128 GB<br/> |                 |
| Windows Web Server 2008 R2                       | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-server-2008"></a>Limites de memória física: Windows Server 2008

A tabela a seguir especifica os limites de memória física para o Windows Server 2008. Os limites maiores que 4 GB para o Windows de 32 bits pressupõem que a [PAE](physical-address-extension.md) está habilitada.



| Versão                                       | Limite em x86     | Limite em x64      | Limite em IA64   |
|-----------------------------------------------|------------------|-------------------|-----------------|
| Windows Server 2008 Datacenter                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 Enterprise                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 HPC Edition               |                  | 128 GB<br/> |                 |
| Windows Server 2008 Standard                  | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Server 2008 for Itanium-Based Systems |                  |                   | 2 TB<br/> |
| Windows Small Business Server 2008            | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Web Server 2008                       | 4 GB<br/>  | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-vista"></a>Limites de memória física: Windows Vista

A tabela a seguir especifica os limites de memória física para o Windows Vista.



| Versão                    | Limite em x86    | Limite em x64      |
|----------------------------|-----------------|-------------------|
| Windows Vista Ultimate     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Enterprise   | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Business     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows Vista Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows Vista Starter      | 1 GB<br/> |                   |



 

## <a name="physical-memory-limits-windows-home-server"></a>Limites de memória física: Windows Home Server

O Windows Home Server está disponível apenas em uma edição de 32 bits. O limite de memória física é de 4 GB.

## <a name="physical-memory-limits-windows-server-2003-r2"></a>Limites de memória física: Windows Server 2003 R2

A tabela a seguir especifica os limites de memória física para o Windows Server 2003 R2. Os limites acima de 4 GB para o Windows de 32 bits pressupõem que a [PAE](physical-address-extension.md) está habilitada.



| Versão                                              | Limite em x86                                 | Limite em x64     |
|------------------------------------------------------|----------------------------------------------|------------------|
| Windows Server 2003 R2 Datacenter Edition<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Enterprise Edition<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-2-sp2"></a>Limites de memória física: Windows Server 2003 com Service Pack 2 (SP2)

A tabela a seguir especifica os limites de memória física para o Windows Server 2003 com Service Pack 2 (SP2). Os limites acima de 4 GB para o Windows de 32 bits pressupõem que a [PAE](physical-address-extension.md) está habilitada.



| Versão                                                                      | Limite em x86                                 | Limite em x64     | Limite em IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|------------------|-----------------|
| Windows Server 2003 com Service Pack 2 (SP2), Datacenter Edition<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 com Service Pack 2 (SP2), Enterprise Edition<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 com Service Pack 2 (SP2), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |                 |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-1-sp1"></a>Limites de memória física: Windows Server 2003 com Service Pack 1 (SP1)

A tabela a seguir especifica os limites de memória física para o Windows Server 2003 com Service Pack 1 (SP1). Os limites acima de 4 GB para o Windows de 32 bits pressupõem que a [PAE](physical-address-extension.md) está habilitada.



| Versão                                                                      | Limite em x86                                 | Limite em x64        | Limite em IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------|-----------------|
| Windows Server 2003 com Service Pack 1 (SP1), Datacenter Edition<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 com Service Pack 1 (SP1), Enterprise Edition<br/> | 64 GB<br/> (16 GB com 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 com Service Pack 1 (SP1), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/>    |                 |



 

## <a name="physical-memory-limits-windows-server-2003"></a>Limites de memória física: Windows Server 2003

A tabela a seguir especifica os limites de memória física para o Windows Server 2003. Os limites acima de 4 GB para o Windows de 32 bits pressupõem que a [PAE](physical-address-extension.md) está habilitada.



| Versão                                                    | Limite em x86                                 | Limite em IA64     |
|------------------------------------------------------------|----------------------------------------------|-------------------|
| Windows Server 2003, Datacenter Edition<br/>         | 64 GB<br/> (16 GB com 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Enterprise Edition<br/>         | 64 GB<br/> (16 GB com 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Standard Edition<br/>           | 4 GB<br/>                              |                   |
| Windows Server 2003, Web Edition<br/>                | 2 GB<br/>                              |                   |
| Windows Small Business Server 2003<br/>              | 4 GB<br/>                              |                   |
| Windows Compute Cluster Server 2003<br/>             |                                              | 32 GB<br/>  |
| Windows Storage Server 2003, Enterprise Edition<br/> | 8 GB<br/>                              |                   |
| Windows Storage Server 2003<br/>                     | 4 GB<br/>                              |                   |



 

## <a name="physical-memory-limits-windows-xp"></a>Limites de memória física: Windows XP

A tabela a seguir especifica os limites de memória física para o Windows XP.



| Versão                    | Limite em x86      | Limite em x64      | Limite em IA64                     |
|----------------------------|-------------------|-------------------|-----------------------------------|
| Windows XP                 | 4 GB<br/>   | 128 GB<br/> | 128 GB (sem suporte)<br/> |
| Windows XP Starter Edition | 512 MB<br/> | N/D<br/>    | N/D<br/>                    |



 

## <a name="physical-memory-limits-windows-embedded"></a>Limites de memória física: Windows Embedded

A tabela a seguir especifica os limites de memória física para o Windows Embedded.



| Versão                                   | Limite em x86    | Limite em x64      |
|-------------------------------------------|-----------------|-------------------|
| Windows XP Embedded<br/>            | 4 GB<br/> |                   |
| Windows Embedded Standard 2009<br/> | 4 GB<br/> |                   |
| Windows Embedded Standard 7<br/>    | 4 GB<br/> | 192 GB<br/> |



 

## <a name="how-graphics-cards-and-other-devices-affect-memory-limits"></a>Como placas gráficas e outros dispositivos afetam os limites de memória

Os dispositivos precisam mapear sua memória abaixo de 4 GB para compatibilidade com versões do Windows que não reconhecem a PAE. Portanto, se o sistema tiver 4 GB de RAM, alguns deles serão desabilitados ou remapeados acima de 4 GB pelo BIOS. Se a memória for remapeada, o Windows x64 poderá usar essa memória. As versões de cliente x86 do Windows não dão suporte à memória física acima da marca de 4 GB, portanto, elas não podem acessar essas regiões remapeadas. Qualquer versão x64 do Windows ou x86 Server pode.

As versões de cliente x86 com PAE habilitado têm um espaço de endereço físico utilizável de 37 bits (128 GB). O limite que essas versões impõem é o endereço de RAM físico mais alto permitido, não o tamanho do espaço de e/s. Isso significa que os drivers com reconhecimento de PAE podem realmente usar o espaço físico acima de 4 GB, se desejarem. Por exemplo, os drivers podem mapear as regiões de memória "perdidas" localizadas acima de 4 GB e expor essa memória como um disco de RAM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ajuste de 4 gigabytes](4-gigabyte-tuning.md)
</dt> <dt>

[**\_reconhecimento de \_ \_ endereço grande de arquivo \_ de imagem**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)
</dt> <dt>

[Extensão de endereço físico](physical-address-extension.md)
</dt> </dl>

 

 
